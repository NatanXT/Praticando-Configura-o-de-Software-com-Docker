# Praticando-Configura-o-de-Software-com-Docker
Atividades e tarefas da faculdade ministradas pelo professor para a familiaridade com o docker.

## Visão Geral

Este ambiente demonstra um fluxo de automação Strapi → n8n → LM Studio → Strapi, onde o sistema é capaz de:

Receber uma nova avaliação de usuário no Strapi.
O n8n detecta o evento via Webhook.
O n8n envia o texto da avaliação para o modelo local Phi-4-Mini executando no LM Studio.
O modelo analisa o sentimento (positivo, negativo, neutro).
O n8n atualiza o registro no Strapi com o campo avaliacao_automatica.

## Estrutura do Projeto

praticando-configura-o-de-software-com-docker
│
├── n8n_data/              # Volume persistente do n8n
│
├── pgdata/                # Banco PostgreSQL do Strapi
│
├── strapi-app/            # Código-fonte do Strapi
│
├── docker-compose.yml     # Configuração principal dos serviços
└── README.md              # Este arquivo

## Acesso as Estruturas

strapi: http://localhost:1337/admin
n8n: http://localhost:5678
