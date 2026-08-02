<div align="center">

# 💰 Speech AI API

API desenvolvida com **Java 21**, **Spring Boot** e **Spring AI** para processamento de comandos de voz e gerenciamento de transações financeiras utilizando Inteligência Artificial.

![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring AI](https://img.shields.io/badge/Spring_AI-412991?style=for-the-badge&logo=spring&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

</div>

---

# 📖 Sobre o projeto

O **Speech AI API** é uma API REST desenvolvida em **Java + Spring Boot** que utiliza os recursos do **Spring AI** para permitir a interação com o sistema por meio de comandos de voz.

A aplicação recebe um arquivo de áudio, converte a fala em texto, utiliza um modelo de Inteligência Artificial para interpretar a intenção do usuário, executa automaticamente o caso de uso correspondente e devolve a resposta em áudio.

Toda a solução foi construída seguindo os princípios de **Clean Architecture** e **Domain-Driven Design (DDD)**, mantendo as regras de negócio desacopladas das tecnologias de infraestrutura.

---

# 🚀 O que o projeto faz

O fluxo principal da aplicação é composto pelas seguintes etapas:

1. Upload de um arquivo de áudio.
2. Conversão da fala em texto utilizando o modelo de transcrição da OpenAI.
3. Interpretação da intenção do usuário através do Spring AI.
4. Seleção automática do caso de uso utilizando **Tool Calling**.
5. Execução das regras de negócio.
6. Geração da resposta em texto.
7. Conversão da resposta para áudio (MP3).
8. Retorno do áudio ao cliente.

As regras de negócio permanecem centralizadas na camada de aplicação, permitindo reutilização tanto pela API REST quanto pelos componentes de Inteligência Artificial.

---

# 🏗 Arquitetura

O projeto segue os princípios da **Clean Architecture**, promovendo baixo acoplamento entre as camadas.

```text
src/main/java
│
├── domain
│   ├── entidades
│   ├── value objects
│   └── contratos de repositório
│
├── application
│   ├── casos de uso
│   ├── serviços
│   └── ferramentas da IA
│
└── infrastructure
    ├── controllers REST
    ├── persistência JPA
    ├── configurações
    └── integrações externas
```

---

# 🛠 Tecnologias utilizadas

<div align="center">

<img src="https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring_AI-412991?style=for-the-badge&logo=spring&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white"/>
<img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white"/>
<img src="https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white"/>
<img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black"/>
<img src="https://img.shields.io/badge/JUnit_5-25A162?style=for-the-badge&logo=junit5&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>

</div>

## Stack utilizada

| Categoria | Tecnologias |
|------------|-------------|
| Linguagem | Java 21 |
| Framework | Spring Boot, Spring AI |
| Persistência | Spring Data JPA, Hibernate |
| Banco de Dados | PostgreSQL |
| Inteligência Artificial | OpenAI, Speech-to-Text, Chat Model, Tool Calling e Text-to-Speech |
| Build | Gradle |
| Testes | JUnit 5 |
| Documentação | Swagger / OpenAPI |
| Containers | Docker |

---

# 🚀 Como instalar e executar

## Pré-requisitos

- Java 21
- Gradle
- PostgreSQL
- Docker (opcional)
- Chave da API da OpenAI

## Clone o projeto

```bash
git clone https://github.com/Joaomacosdev/speechai.git
```

```bash
cd speechai
```

## Configure a variável de ambiente

### Linux / macOS

```bash
export OPENAI_API_KEY="SUA_CHAVE"
```

### Windows (PowerShell)

```powershell
$env:OPENAI_API_KEY="SUA_CHAVE"
```

## Execute a aplicação

```bash
./gradlew bootRun
```

## Execute os testes

```bash
./gradlew test
```

---

# 📖 Documentação da API

Após iniciar a aplicação, acesse:

```
http://localhost:8080/swagger-ui/index.html
```

---

# 📸 Screenshots

Adicione imagens do projeto na pasta `docs/images`.

### Tela inicial

```
docs/images/home.png
```

### Upload de áudio

```
docs/images/upload-audio.png
```

### Resposta da IA

```
docs/images/response.png
```

---

# 🌐 Deploy

Atualmente o projeto está em desenvolvimento e ainda não possui uma versão publicada.

---

# ⚙️ Funcionalidades

- Upload de arquivos de áudio
- Conversão de voz para texto
- Interpretação de linguagem natural
- Tool Calling com Spring AI
- Cadastro de transações financeiras
- Consulta de transações
- Conversão de texto para áudio
- Arquitetura baseada em Clean Architecture e DDD
- Documentação automática com Swagger

---

# 🧩 Desafios enfrentados

## Integração da IA com as regras de negócio

O principal desafio foi integrar o Spring AI sem acoplar a Inteligência Artificial diretamente ao domínio.

A solução foi utilizar o recurso de **Tool Calling**, expondo apenas os casos de uso da camada de aplicação. Dessa forma, o modelo pode executar funcionalidades do sistema sem acessar diretamente as regras de negócio.

## Processamento de áudio

Foi necessário implementar um fluxo completo de entrada e saída de áudio.

Esse fluxo utiliza:

- Speech-to-Text
- Chat Model
- Tool Calling
- Text-to-Speech

Tudo de forma integrada através do Spring AI.

## Organização da arquitetura

Outro desafio foi manter a arquitetura utilizada durante todo o projeto, garantindo separação entre domínio, aplicação e infraestrutura, facilitando manutenção, testes e evolução da aplicação.

---

# 📚 Referências

- Spring Boot
- Spring AI
- Spring Data JPA
- Hibernate
- PostgreSQL
- OpenAI API
- Swagger / OpenAPI
- Clean Architecture
- Domain-Driven Design (DDD)

---

# 📂 Repositório

https://github.com/Joaomacosdev/speechai

---

# 👨‍💻 Autor

**João Marcos Santos Aragão**

Desenvolvedor Back-end Java apaixonado por arquitetura de software, APIs REST, Spring Boot e Inteligência Artificial.

- GitHub: https://github.com/Joaomacosdev
- LinkedIn: https://www.linkedin.com/in/joaomarcosaragao/

