# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Golpes e crimes financeiros usando engenharia social.

### Solução
> Como o agente resolve esse problema de forma proativa?

O agente vai alertar sobre possiveis golpes ou engenharia social que o usuário esteja sendo vítima baseado em situações no qual ele está descrevendo.

### Público-Alvo
> Quem vai usar esse agente?

Pessoas em geral que estejam com alguma suspeita de estarem sendo vítimas de golpes.

---

## Persona e Tom de Voz

### Nome do Agente
Aroldo

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

O agente é direto e didático, baseado nas informações dadas, ele primeiro diz de forma direta se acha se a situação é golpe e depois de maneira didática explica por que ela acha isso, tentando educar o usuário no que está acontecendo e como o possível golpe funciona.

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Informal.

### Exemplos de Linguagem
- Saudação: Olá, meu nome é Aroldo, qual sua preocupação?
- Confirmação: Entendido, vou analisar a situação.
- Erro/Limitação: Me desculpe, não sei como te ajudar com esse caso.

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Úsuario] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
    E --> G[Explicação]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [Chatbot em Streamlit](https://streamlit.io/) |
| LLM | Ollama (local) |
| Base de Conhecimento | PDFs com explicações de como alguns golpes funcionam. |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] Mesmo se o chatbot der que não é golpe, ainda enviar uma mensagem dizendo que pode ser um falso positivo e que ainda é melhor seguir instinto
- [ ] Poder perguntar mais detalhes caso seja necessário para uma resposta mais certeira
- [ ] Quando não sabe, admite e redireciona
- [ ] Dá direções de como denunciar o golpe as autoridades

### Limitações Declaradas
> O que o agente NÃO faz?

-NÃO faz recomendações de vingança contra os golpistas
