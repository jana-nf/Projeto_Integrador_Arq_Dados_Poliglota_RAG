# Arquitetura de Dados Poliglota com RAG: Interface de Linguagem Natural para Consultas Híbridas (SQL, NoSQL & Vector DB)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PostgreSQL](https://img.shields.io/badge/postgresql-%23336791.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991.svg?style=for-the-badge&logo=openai&logoColor=white)

## 📌 Visão Geral

Este projeto foi desenvolvido como **Projeto Integrador** para o curso de Tecnologia em Banco de Dados. O objetivo central é resolver o gargalo de acesso a dados em empresas de E-commerce, através de uma solução de **Business Intelligence (BI) Cognitivo**permitindo que gestores sem conhecimento técnico extraiam insights estratégicos utilizando linguagem natural.

A solução baseia-se no conceito de **Persistência Poliglota**, utilizando o banco de dados ideal para cada tipo de carga de trabalho, e utiliza a técnica de **RAG (Retrieval-Augmented Generation)** para conectar uma LLM (IA) aos dados privados da empresa.

## 🛠️ Stack Tecnológica
- **Relacional (PostgreSQL):** Dados transacionais e financeiros (ACID).
- **Documental (MongoDB):** Dados semiestruturados e reviews de produtos.
- **Vetorial (ChromaDB/Pinecone):** Busca semântica baseada em embeddings de texto.
- **Orquestração:** Python + LangChain.
- **IA:** OpenAI API (GPT-4 / Text-Embeddings).
- **Interface:** Streamlit.

## 📐 Arquitetura do Sistema
O sistema opera através de três camadas de dados coordenadas por um Agente de IA:
1. **Camada de Fatos:** Consulta SQL no PostgreSQL para métricas exatas.
2. **Camada de Contexto:** Busca semântica no Vector DB para entender intenções e sentimentos.
3. **Camada de Documentos:** Recuperação de detalhes técnicos no MongoDB.

## 📚 Fundamentação Teórica
O projeto implementa as teses de **Scott Leberknight (2008)** sobre a necessidade de sistemas poliglotas, onde a eficiência é alcançada ao não forçar todos os dados em um único modelo relacional. A camada de IA atua como o "tradutor universal" que resolve a complexidade de integração dessas fontes.
