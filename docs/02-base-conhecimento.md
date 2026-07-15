# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `A Study of Social Engineering in Online Frauds.pdf` | PDF| Entendimento de como funciona a engenharia social |
| `Cryptocurrency_Scams_Analysis_and_Perspectives.pdf` | PDF | Entendimento sobre golpes envolvendo crypto moedas |
| `cybercrime,scamsAndTheirVictims.pdf` | PDF | Entender sobre as vitimas de golpes de crimes cibernéticos|
| `Phishing Attacks: A Recent Comprehensive Study and a New Anatomy.pdf` | PDF | Estudo especializado em ataques usando phising |
| `romance scams.txt` | TXT | Uma compreensão de como golpes de romance funcionam|
| `Scams-Schemes-Swindles-FINAL-On-Website.pdf` | PDF | Funcionamento de golpes|
| `Social Engineering Attacks Prevention: A Systematic Literature Review.pdf` | PDF | Entendimento de prevenções de ataques de engenharia social|
| `Social Engineering - the Art of Human Hacking.pdf` | PDF | Livro sobre engenharia social|
| `social enginnering and scams related.txt` | PDF | Entendimento de diferentes tipos de golpes e ataques no qual engenharia social é usado|

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

[ Os PDF/TXT são carregados no início da sessão e incluídos no contexto do prompt]

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Os dados são consultados dinamicamente

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Situação em que o usuário se encontra: O banco me ligou me pedindo diversos dados como senhas, cpf e respostas de senhas que coloquei lá.
...
```
