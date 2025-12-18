# Democratização do BI: Interface de Linguagem Natural para Consultas Híbridas (SQL & NoSQL)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PostgreSQL](https://img.shields.io/badge/postgresql-%23336791.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991.svg?style=for-the-badge&logo=openai&logoColor=white)

## 📌 Sobre o Projeto
Este projeto foi desenvolvido como **Projeto Integrador** para o curso de Tecnologia em Banco de Dados. O objetivo central é solucionar o gargalo de acesso a dados em empresas de E-commerce, permitindo que gestores sem conhecimento técnico extraiam insights estratégicos utilizando linguagem natural.

A solução utiliza **IA Generativa** para interpretar perguntas em português e decidir, de forma autônoma, se deve consultar dados transacionais no **PostgreSQL** ou dados flexíveis (reviews e catálogos) no **MongoDB**.

## 🚀 Diferenciais Técnicos
* **Persistência Poliglota:** Integração em tempo real entre bancos relacionais e não-relacionais.
* **Modern Data Stack (MDS):** Foco em agilidade, descentralização e redução do *time-to-insight*.
* **Segurança (Least Privilege):** Agente de IA configurado com permissões de apenas leitura para garantir a integridade dos dados.
* **Arquitetura de Agentes:** Uso de LangChain para orquestrar a decisão de rotas entre as diferentes fontes de dados.

## 📚 Fundamentação Teórica
O projeto baseia-se no conceito de **Polyglot Persistence**, termo cunhado por **Scott Leberknight** em 2008. 
A arquitetura utiliza o banco de dados ideal para cada tipo de carga de trabalho:
- **PostgreSQL**: Para dados transacionais e consistência.
- **MongoDB**: Para dados semiestruturados e escalabilidade de leitura.
O diferencial desta implementação é o uso de **IA Generativa** para abstrair a complexidade de consultar esses múltiplos motores.

## 🛠️ Arquitetura do Sistema
O fluxo de dados segue a seguinte lógica:
1. O usuário faz uma pergunta (ex: "Qual o faturamento do produto mais bem avaliado?").
2. O **LLM Agent** analisa o schema do PostgreSQL e as coleções do MongoDB.
3. A IA gera e executa o **SQL** e o **MQL** (Mongo Query Language).
4. O Python consolida os resultados e apresenta uma resposta amigável.

## 📊 Estrutura de Dados
### Relacional (PostgreSQL)
* `clientes`: Dados cadastrais.
* `vendas`: Transações e faturamento.
* `itens_venda`: Detalhamento dos pedidos.

### NoSQL (MongoDB)
* `catalogo_produtos`: Atributos técnicos variáveis.
* `reviews`: Avaliações qualitativas e notas de usuários.

## 🔧 Como Executar
1. Clone o repositório:
   ```bash
   git clone [https://github.com/jana-nf/Projeto_Integrador_DemoBI_LLM_Persistencia_Poliglota](https://github.com/jana-nf/Projeto_Integrador_DemoBI_LLM_Persistencia_Poliglota/tree/main)
