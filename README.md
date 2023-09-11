# Santander Dev Week 2023 - ETL com Python

Este é um repositório para um projeto da Santander Dev Week 2023, onde o objetivo é criar mensagens de marketing personalizadas para envolver os clientes de maneira mais eficaz. Neste projeto, usaremos a IA Generativa e a API da Santander Dev Week para realizar essa tarefa.

## Contexto

Você é um cientista de dados no Santander e recebeu a tarefa de envolver seus clientes de maneira mais personalizada. Seu objetivo é usar o poder da IA Generativa para criar mensagens de marketing personalizadas que serão entregues a cada cliente.

## Condições do Problema

1. Você recebeu uma planilha simples em formato CSV ('SDW2023.csv') com uma lista de IDs de usuário do banco.
2. Seu trabalho é consumir o endpoint GET https://sdw-2023-prd.up.railway.app/users/{id} (API da Santander Dev Week 2023) para obter os dados de cada cliente.
3. Depois de obter os dados dos clientes, você usará a API do ChatGPT (OpenAI) para gerar uma mensagem de marketing personalizada para cada cliente. Essa mensagem deve enfatizar a importância dos investimentos.
4. Uma vez que a mensagem para cada cliente esteja pronta, você enviará essas informações de volta para a API, atualizando a lista de "news" de cada usuário usando o endpoint PUT https://sdw-2023-prd.up.railway.app/users/{id}.

## Passos Realizados

### Extract

Extraímos a lista de IDs de usuário a partir do arquivo CSV ('SDW2023.csv'). Para cada ID, fizemos uma requisição GET para obter os dados do usuário correspondente.

### Transform

Utilizamos a API do OpenAI GPT-4 para gerar uma mensagem de marketing personalizada para cada usuário. Substituímos o texto "api" pela API Key da OpenAI.

### Load

Atualizamos a lista de "news" de cada usuário na API com a nova mensagem gerada.

## Como executar o código

1. Clone este repositório.
2. Certifique-se de ter as bibliotecas necessárias instaladas, como pandas, requests e openai. Você pode instalá-las usando `pip install pandas requests openai`.
3. Substitua a variável `openai_api_key` pelo sua própria API Key da OpenAI.
4. Execute o código em um ambiente Python.

## Documentação da API (Swagger)

https://sdw-2023-prd.up.railway.app/swagger-ui.html

Esta API ficará disponível no Railway por um período de tempo limitado, mas este é um código-fonte aberto.