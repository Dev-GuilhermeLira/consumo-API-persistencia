# Consumo de API e Persistência em Arquivo

Atividade 02 da disciplina **Java II — Tópicos Avançados**, da Pós-Graduação em Desenvolvimento Java.

**Cotador de moedas** que lê um arquivo de entrada, consome uma **API REST externa** para obter as cotações e grava os resultados em um arquivo **CSV**. O projeto trabalha comunicação HTTP, JSON, programação assíncrona e manipulação de arquivos.

## 🧠 Conceitos aplicados

- Consumo de API REST externa com o `HttpClient` do Java moderno
- Requisições HTTP para obter informações de moedas
- Processamento de respostas em JSON
- Programação assíncrona com `CompletableFuture` e composição de operações assíncronas
- Tratamento de exceções
- Leitura de arquivo de entrada e geração de arquivo de saída em **CSV**
- Uso de `LocalDateTime`
- Testes automatizados com **Mockito** para criação de mocks
- Gerenciamento do projeto com **Maven**

## 💱 Cenários de teste

Exemplos de moedas usadas nos testes:

```text
BRL
ABC
EUR
GBP
JPY
```

O projeto também cobre cenários de erro, como códigos de moeda inválidos (por exemplo, `ABC`) e falhas durante a comunicação ou o processamento.

## 🔄 Fluxo da aplicação

```text
Arquivo de entrada
       ↓
Leitura das moedas
       ↓
Consumo da API REST
       ↓
Processamento da resposta
       ↓
Tratamento de erros
       ↓
Geração do resultado
       ↓
Arquivo CSV
```

## 🛠️ Tecnologias

Java · Maven · JUnit · Mockito · HttpClient · IntelliJ IDEA · Git · GitHub

## 🗂️ Estrutura do projeto

```text
.
├── entrada/
├── src/
├── pom.xml
└── README.md
```

## ▶️ Como executar

O projeto pode ser aberto no **IntelliJ IDEA** como projeto Maven, ou executado pelo Maven Wrapper.

Executar os testes:

```bash
# Windows
mvnw.cmd test

# Linux / macOS
./mvnw test
```

Compilar o projeto:

```bash
# Windows
mvnw.cmd clean package

# Linux / macOS
./mvnw clean package
```

Como o projeto consome uma API externa, é necessário ter conexão com a internet para executar a aplicação. Os testes usam mocks. Os diretórios `target/` e os arquivos da IDE não são versionados, conforme o `.gitignore`.

## 🎯 Objetivo acadêmico

Aplicar na prática conceitos de **integração entre sistemas**, **programação assíncrona** e **persistência em arquivos**.

Este repositório faz parte do portfólio acadêmico da Pós-Graduação em Desenvolvimento Java.
