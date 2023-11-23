# Santander Dev Week 2023 (ETL com Python)
Contexto: Você é um cientista de dados no Santander e recebeu a tarefa de envolver seus clientes de maneira mais personalizada. Seu objetivo é usar o poder da IA Generativa para criar mensagens de marketing personalizadas que serão entregues a cada cliente.

## Condições do Problema:

Você recebeu uma planilha simples, em formato CSV ('SDW2023.csv'), com uma lista de IDs de usuário do banco.

Seu trabalho é consumir o endpoint GET https://sdw-2023-prd.up.railway.app/users/{id} (API da Santander Dev Week 2023) para obter os dados de cada cliente.
Depois de obter os dados dos clientes, você vai usar a API do ChatGPT (OpenAI) para gerar uma mensagem de marketing personalizada para cada cliente. Essa mensagem deve enfatizar a importância dos investimentos.
Uma vez que a mensagem para cada cliente esteja pronta, você vai enviar essas informações de volta para a API, atualizando a lista de "news" de cada usuário usando o endpoint PUT https://sdw-2023-prd.up.railway.app/users/{id}.

* Repositório da API: https://github.com/digitalinnovationone/santander-dev-week-2023-api
sdw2023_api_url = 'https://sdw-2023-prd.up.railway.app'
 
```json    
[
  {
    "id": 3827,
    "name": "Luna",
    "account": {
      "id": 4062,
      "number": "02023-7",
      "agency": "0001",
      "balance": 0.0,
      "limit": 500.0
    },
    "card": {
      "id": 3719,
      "number": "**** **** **** 0423",
      "limit": 1000.0
    },
    "features": [],
    "news": [
      {
        "id": 8078,
        "icon": "https://digitalinnovationone.github.io/santander-dev-week-2023-api/icons/credit.svg",
        "description": "O Santander tem solu\u00e7\u00f5es de cr\u00e9dito sob medida pra voc\u00ea. Confira!"
      },
      {
        "id": 8079,
        "icon": "https://digitalinnovationone.github.io/santander-dev-week-2023-api/icons/credit.svg",
        "description": "Invista hoje para um futuro pr\u00f3spero! #InvistaComSabedoria"
      }
    ]
  },
  {
    "id": 3831,
    "name": "Matheus",
    "account": {
      "id": 4066,
      "number": "02023-1",
      "agency": "0001",
      "balance": 0.0,
      "limit": 500.0
    },
    "card": {
      "id": 3723,
      "number": "**** **** **** 0428",
      "limit": 1000.0
    },
    "features": [],
    "news": [
      {
        "id": 8080,
        "icon": "https://digitalinnovationone.github.io/santander-dev-week-2023-api/icons/credit.svg",
        "description": "O Santander tem solu\u00e7\u00f5es de cr\u00e9dito sob medida pra voc\u00ea. Confira!"
      },
      {
        "id": 8081,
        "icon": "https://digitalinnovationone.github.io/santander-dev-week-2023-api/icons/credit.svg",
        "description": "Invista no seu futuro, Matheus. Fa\u00e7a seu dinheiro trabalhar por voc\u00ea."
      }
    ]
  },
  {
    "id": 3832,
    "name": "Leni",
    "account": {
      "id": 4067,
      "number": "02023-5",
      "agency": "0001",
      "balance": 0.0,
      "limit": 500.0
    },
    "card": {
      "id": 3724,
      "number": "**** **** **** 0412",
      "limit": 1000.0
    },
    "features": [],
    "news": [
      {
        "id": 8082,
        "icon": "https://digitalinnovationone.github.io/santander-dev-week-2023-api/icons/credit.svg",
        "description": "O Santander tem solu\u00e7\u00f5es de cr\u00e9dito sob medida pra voc\u00ea. Confira!"
      },
      {
        "id": 8083,
        "icon": "https://digitalinnovationone.github.io/santander-dev-week-2023-api/icons/credit.svg",
        "description": "Invista hoje, colha amanh\u00e3!"
      }
    ]
  }
]
```
### Transform
Utilize a API do OpenAI GPT-4 para gerar uma mensagem de marketing personalizada para cada usuário.

* Documentação Oficial da API OpenAI: https://platform.openai.com/docs/api-reference/introduction
* Informações sobre o Período Gratuito: https://help.openai.com/en/articles/4936830

#### Mensagem gerada pela IA generativa
```
Invista no seu futuro financeiro!
Invista no seu futuro! Seja inteligente financeiramente.
Invista hoje, colha amanhã! #InvestimentosEssenciais
Load
Atualize a lista de "news" de cada usuário na API com a nova mensagem gerada.
```

<hr>

[![Linkedin Badge](https://img.shields.io/badge/-JeanCarlo-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/jeancarlotorre619b/)](https://www.linkedin.com/in/jeancarlotorre619b/)

<h3>Contribuindo</h3>

⭐️ Star o projeto

🐛 Encontrar e relatar issues
