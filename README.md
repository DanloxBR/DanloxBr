👨‍💻 Daniel Santos Oliveira

Java Backend Developer | Spring Boot | APIs REST | Microsserviços | Kafka

Desenvolvedor Backend Java com foco na construção de APIs, sistemas distribuídos e aplicações orientadas a boas práticas de engenharia de software.

Tenho experiência prática com Java, Spring Boot, Spring Data JPA, Hibernate, PostgreSQL, APIs REST, Spring Security, JWT, Apache Kafka, microsserviços, Docker, Kubernetes, CI/CD, JUnit e Mockito.

Meu foco é transformar problemas de negócio em soluções organizadas, seguras, escaláveis e fáceis de manter.

🚀 Sobre mim

☕ Desenvolvimento Backend com Java 8/17

🌱 Spring Boot e desenvolvimento de APIs REST

🗄️ PostgreSQL, SQL, JPA e Hibernate

🔄 Apache Kafka e comunicação assíncrona

🔐 Spring Security e JWT

🧪 JUnit e Mockito

🐳 Docker e Kubernetes

⚙️ CI/CD, Git e GitHub

🤖 Automação e RPA com Java + Selenium

🏗️ Arquitetura em camadas, Clean Code e SOLID

📚 Estudos contínuos em microsserviços, arquitetura e sistemas distribuídos

🛠️ Tech Stack

Backend







Banco de Dados




DevOps






Testes




⭐ Projetos em Destaque

🤖 Telegram Support Bot

<p align="center">
  <strong>Sistema de atendimento e gerenciamento de chamados integrado ao Telegram.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-8-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white">
  <img src="https://img.shields.io/badge/Spring%20Boot-2.7.18-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/Telegram-26A5E5?style=for-the-badge&logo=telegram&logoColor=white">
</p>

Aplicação backend desenvolvida em Java 8 + Spring Boot, utilizando o Telegram como canal de atendimento e o PostgreSQL para persistência dos dados.

O sistema foi projetado para representar um cenário real de suporte, com clientes, atendentes, chamados, perfis de acesso, notificações e regras de negócio.

✨ Principais funcionalidades

Cliente

Atendente

Sistema

Abrir chamados

Visualizar chamados pendentes

Controle de perfis

Consultar chamados

Assumir chamados

Controle de permissões

Acompanhar status

Resolver chamados

Notificações automáticas

Visualizar detalhes

Cancelar chamados

Persistência PostgreSQL

Consultar conta

Acompanhar atendimentos

Optimistic Locking

🔄 Fluxo de atendimento

                    ┌─────────────┐
                    │   CLIENTE   │
                    └──────┬──────┘
                           │
                           │ Abre chamado
                           ▼
                    ┌─────────────┐
                    │    ABERTO   │
                    └──────┬──────┘
                           │
                           │ Notificação
                           ▼
                    ┌─────────────┐
                    │  ATENDENTE  │
                    └──────┬──────┘
                           │
                           │ Assume
                           ▼
                 ┌──────────────────┐
                 │  EM_ATENDIMENTO  │
                 └────────┬─────────┘
                          │
                    ┌─────┴─────┐
                    │           │
                 Resolver    Cancelar
                    │           │
                    ▼           ▼
              ┌──────────┐ ┌───────────┐
              │ RESOLVIDO│ │ CANCELADO │
              └──────────┘ └───────────┘

👥 Perfis de acesso

CLIENTE
  └── Gerencia os próprios chamados

ATENDENTE
  └── Gerencia os chamados de atendimento

ADMIN
  └── Possui permissões administrativas
      e pode atuar no atendimento

🔐 Controle de concorrência

O sistema utiliza Optimistic Locking através do @Version, reduzindo o risco de alterações conflitantes quando mais de um atendente tenta modificar o mesmo chamado.

@Version
@Column(nullable = false)
private Long version;

🏗️ Arquitetura

Telegram
    │
    ▼
┌─────────────────────┐
│     SupportBot      │
│ Mensagens / Menus   │
│ Callbacks / Ações   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│       Service       │
│ Regras de negócio   │
│ Validações          │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│     Repository      │
│ Spring Data JPA     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│     PostgreSQL      │
└─────────────────────┘

🛠️ Stack tecnológica

Java 8
Spring Boot 2.7.18
Spring Data JPA
Hibernate
PostgreSQL
Telegram Bot API
Maven
Lombok
Git
GitHub

📐 Conceitos aplicados

Arquitetura em camadas

Programação Orientada a Objetos

Injeção de dependências

Separação de responsabilidades

Regras de negócio

Controle de acesso

Persistência com JPA/Hibernate

Tratamento de exceções

Optimistic Locking

Integração com serviço externo

Versionamento com Git/GitHub

📂 Estrutura

src/main/java/br.com.danieldev.supportbot
│
├── bot
├── config
├── entity
├── enums
├── repository
└── service

▶️ Execução

Requisitos:

Java 8

Maven

PostgreSQL

Bot criado no Telegram

Clone:

git clone https://github.com/DanloxBR/bot-telegram-java.git
cd bot-telegram-java

Crie o banco:

CREATE DATABASE supportbot;

Configure as credenciais do PostgreSQL e o token do Telegram através de variáveis de ambiente.

Compile:

mvn clean install

Execute:

mvn spring-boot:run

🔒 Segurança

Não versionar:

Tokens do Telegram
Senhas do PostgreSQL
Chaves de API
Credenciais

Utilize variáveis de ambiente para informações sensíveis.

🚀 Roadmap

Docker e Docker Compose

CI/CD

Testes unitários e de integração

Logs estruturados

Monitoramento

Dashboard administrativo

Métricas de atendimento

Histórico de alterações

SLA de atendimento

Priorização de chamados

Categorias de atendimento

Projeto desenvolvido como aplicação prática de backend Java, com foco em integração, regras de negócio, persistência e arquitetura.

🩺 Fisioterapia Manager

Sistema desktop para gerenciamento de clínicas e atendimentos de fisioterapia, desenvolvido com foco em uma necessidade real de negócio.

Permite centralizar pacientes, fisioterapeutas, avaliações, sessões, exercícios, agendamentos e dashboards em uma única aplicação.

🚀 Funcionalidades

👤 Gestão de pacientes

🧑‍⚕️ Gestão de fisioterapeutas

📋 Avaliações fisioterapêuticas

📅 Agendamentos

🏋️ Cadastro e gerenciamento de exercícios

📝 Registro de sessões

📊 Dashboard com indicadores e gráficos

🔐 Autenticação e controle de acesso

🛠️ Tecnologias

Java 8 Spring Boot 2.7.18 Java Swing FlatLaf MigLayout PostgreSQL JFreeChart JPA/Hibernate Lombok Maven Git

🏗️ Conceitos aplicados

Arquitetura em camadas

Separação de responsabilidades

Programação Orientada a Objetos

Persistência de dados

Regras de negócio

Autenticação e controle de acesso

Desenvolvimento de interface desktop

Dashboard e visualização de dados

Versionamento com Git/GitHub

🏦 Bank Account API

API REST bancária desenvolvida em Java e Spring Boot para simulação de operações financeiras.

Permite realizar operações relacionadas a contas bancárias, depósitos, saques, transferências e extratos, com autenticação e controle de acesso.

🚀 Funcionalidades

🔐 Autenticação

🏦 Gerenciamento de contas

💰 Depósitos

💸 Saques

🔄 Transferências

📄 Extrato bancário

🛠️ Tecnologias

Java Spring Boot Spring Security JWT PostgreSQL

💳 API de Pagamentos

API REST desenvolvida para gerenciamento de pagamentos e carteiras digitais, aplicando conceitos de persistência, regras de negócio e desenvolvimento de APIs.

🚀 Funcionalidades

💳 Criação de carteiras

💰 Consulta de saldo

💸 Pagamentos

🔄 Transferências

📜 Histórico de transações

📚 Documentação da API com Swagger/OpenAPI

🛠️ Tecnologias

Java 8 Spring Boot Spring Data JPA PostgreSQL Swagger/OpenAPI

💰 Wallet API

API REST de carteira digital desenvolvida com Java e Spring Boot.

O projeto aborda operações financeiras e gerenciamento de usuários, utilizando autenticação para proteger os recursos da aplicação.

🚀 Funcionalidades

👤 Gerenciamento de usuários

💳 Criação de carteiras

🔄 Transferências

💰 Consulta de saldo

📜 Histórico financeiro

🔐 Autenticação com JWT

🛠️ Tecnologias

Java 8 Spring Boot JPA REST JWT

⭐ API Review Manager

API REST para gerenciamento de avaliações, desenvolvida com foco em organização arquitetural, segurança e regras de negócio.

🏗️ Conceitos aplicados

DTOs

Arquitetura Controller → Service → Repository

Multi-tenancy

Autenticação e autorização

Validação de regras de negócio

Tratamento global de exceções

Persistência com PostgreSQL

🛠️ Tecnologias

Java Spring Boot JPA Hibernate PostgreSQL JWT

🔐 Auth System

Sistema de autenticação e gerenciamento de usuários desenvolvido para praticar Spring Security, JWT e controle de acesso.

🚀 Funcionalidades

👤 Registro de usuários

🔑 Login

🔐 Autenticação com JWT

🛡️ Roles e permissões

🔒 Spring Security

⚠️ Tratamento global de exceções

🛠️ Tecnologias

Java 8 Spring Boot 2.7 Spring Security JWT PostgreSQL

💬 Chat em Tempo Real

Aplicação de comunicação em tempo real desenvolvida para explorar WebSocket, STOMP e comunicação assíncrona.

🚀 Funcionalidades

💬 Comunicação bidirecional

⚡ Mensagens em tempo real

🔌 WebSocket

📡 STOMP

🔄 Integração com mensageria

🛠️ Tecnologias

Java 8 Spring Boot WebSocket STOMP Apache Kafka

🤖 Automação & RPA

🤖 RPA

Projeto desenvolvido para automação de tarefas repetitivas utilizando Java e Selenium.

🛠️ Tecnologias

Java Selenium Maven

⚙️ Automation

Projeto de automação desenvolvido com Selenium WebDriver, aplicando uma estrutura organizada para execução de tarefas automatizadas.

🏗️ Conceitos aplicados

Selenium WebDriver

Factory Pattern

Explicit Waits

Organização e reutilização de componentes

🛠️ Tecnologias

Java Selenium WebDriver Maven Factory Pattern

🤖 RoboValidador

Automação desenvolvida para leitura, validação e geração de relatórios a partir de arquivos de dados.

🚀 Funcionalidades

📄 Leitura de arquivos .txt

📊 Processamento de arquivos .csv

🔎 Validação de informações

📋 Geração de relatórios

🛠️ Tecnologias

Java CSV TXT POO

📊 CSV Selenium Automation

Projeto de automação que utiliza Selenium para extrair informações de uma tabela HTML e gerar um arquivo CSV.

🛠️ Tecnologias

Java 8 Selenium WebDriver OpenCSV Maven

🌐 Web Scraping

Projeto desenvolvido para praticar Web Scraping em Java, realizando a extração de informações de páginas HTML.

🛠️ Tecnologias

Java Jsoup Maven

🖥️ Aplicações Desktop

🧩 Sudoku

Jogo de Sudoku desenvolvido em Java Swing para praticar lógica de programação, eventos e organização de responsabilidades entre interface e regras de negócio.

🛠️ Conceitos

Java Swing

Programação Orientada a Objetos

Eventos e Listeners

Clean Code

Lógica de programação

🛠️ Tecnologias

Java Swing

📱 iPhone — Modelagem POO

Projeto desenvolvido para representar funcionalidades de um iPhone utilizando conceitos fundamentais de Programação Orientada a Objetos.

🏗️ Conceitos aplicados

Interfaces

Abstração

Polimorfismo

Organização em pacotes

🛠️ Tecnologia

Java 8

⌨️ Escape Button

Projeto desenvolvido para estudar eventos, desacoplamento e o padrão Observer/Listener utilizando Java.

🏗️ Conceitos aplicados

Programação Orientada a Objetos

Observer

Listener

Eventos

Desacoplamento

🛠️ Tecnologia

Java

🧮 Calculadora

Aplicação simples desenvolvida para praticar os fundamentos da linguagem Java e a construção de interfaces e operações básicas.

🛠️ Tecnologia

Java

🌐 Frontend

💻 Projeto HTML — Portfólio

Projeto desenvolvido com HTML5 e CSS3, utilizado para praticar construção de páginas web e apresentação de informações profissionais.

🛠️ Tecnologias

HTML5 CSS3

🧪 Projetos de Estudo

📚 Estudos

Repositório utilizado para registrar exercícios, experimentos e estudos relacionados ao ecossistema Java.

📖 Conteúdos

Java

Spring Boot

Maven

Selenium

RPA

Clean Code

Testes

Versionamento

📊 CSV

Projeto de automação envolvendo extração de dados de páginas web e geração de arquivos CSV, utilizando Selenium e OpenCSV.

🛠️ Tecnologias

Java 8 Selenium WebDriver OpenCSV Maven

💵 Finance

API REST voltada para controle financeiro, desenvolvida com Java e Spring Boot.

🚀 Funcionalidades

💰 Cadastro de receitas

💸 Cadastro de despesas

🗂️ Categorias

📊 Cálculo de saldo

✅ Validação de dados

⚠️ Tratamento global de exceções

📦 Respostas padronizadas

🛠️ Tecnologias

Java Spring Boot Spring Data JPA PostgreSQL Lombok

🏗️ Conceitos aplicados

DTOs

Controller

Service

Repository

Validação de dados

Spring Security

Tratamento de regras de negócio

🛠️ Tecnologias

Java 8 Spring Boot Spring Data JPA Spring Security H2 ViaCEP Maven

☕ "Não é sobre conhecer todas as tecnologias. É sobre saber resolver problemas com elas."
