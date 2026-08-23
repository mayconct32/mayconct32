# Hi 👋, I'm Maycon Corrêa

🚀 **Backend Developer | Python & APIs REST**
🇧🇷 Minas Gerais, Brasil

Eu construo **APIs REST escaláveis** com Python, trabalhando com autenticação, bancos de dados relacionais e não relacionais, cache e containerização.
Também dedico parte do tempo a **estudar e documentar livros técnicos** (algoritmos e design de código) direto no GitHub, como forma de fixar o aprendizado na prática.

---

## 🌐 Where to find me

<p align="left">
  <a href="https://github.com/mayconct32">
    <img src="https://img.shields.io/badge/GitHub-MAYCONCT32-181717?style=for-the-badge&logo=github" />
  </a>
  <a href="mailto:maycon326754@gmail.com">
    <img src="https://img.shields.io/badge/Email-maycon326754%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>

---

## 🧠 What I do

- 🔐 APIs REST com autenticação JWT e autorização por dono do recurso
- 🗄️ Modelagem de dados com bancos relacionais (MySQL, PostgreSQL) e não relacionais (MongoDB, Redis)
- ⚡ Cache com Redis, WebSocket em tempo real e rate limiting para proteger endpoints
- 🐳 Containerização de aplicações com Docker / Docker Compose
- 🔌 Integração com serviços externos (Google Gemini, Correios) e migrations de banco com SQLAlchemy + Alembic
- 🧮 Pipelines de RAG com LangChain e bancos vetoriais aplicados a projetos de IA
- 🧪 Testes automatizados com pytest, Testcontainers (banco real em container) e factories de dados
- 📚 Estudo e documentação de livros técnicos (algoritmos, design de código)

---

## 🛠️ Tech Stack

### Backend & APIs

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)


### Dados & Cache

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-2D2D2D?style=for-the-badge&logo=sqlalchemy&logoColor=white)

### DevOps & Tools

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Poetry](https://img.shields.io/badge/Poetry-60A5FA?style=for-the-badge&logo=poetry&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

### Testes & qualidade

![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-16A34A?style=for-the-badge&logo=docker&logoColor=white)



### Em expansão (usadas em alguns projetos, ainda em consolidação)

![JavaScript](https://img.shields.io/badge/JavaScript-FFD43B?style=for-the-badge&logo=javascript&logoColor=000)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)

---

## 📌 Projetos em destaque

### 🍳 [receitas_api](https://github.com/mayconct32/receitas_api) 
API REST em **Python + FastAPI** para compartilhamento de receitas entre chefs, com autenticação JWT, banco de dados poliglota (MySQL + MongoDB), cache com Redis e rate limiting com SlowAPI. Roda via Docker Compose (API + MySQL + MongoDB + Redis) ou local com Poetry + Uvicorn. Documentação interativa via Swagger (`/docs`) e versionamento por URL (`/v1`).

### 💬 [chat_app](https://github.com/mayconct32/chat_app)
Aplicação de **chat em tempo real** construída com **Express.js + MongoDB + Socket.io**, com autenticação JWT e gerenciamento de usuários.

- **Autenticação e autorização**: login gera JWT (`POST /auth`, HS256), cada usuário só acessa os próprios dados via middleware `verify_permission`.
- **WebSocket com autenticação**: conexão ao Socket.io exige token JWT; mensagens sanitizadas contra XSS (`sanitize-html`), limitadas a 250 caracteres.
- **CRUD de usuários**: criação, consulta, atualização e remoção, com validação via `express-validator` (senha 8+ caracteres, username/email únicos).
- **Segurança**: hash de senha com bcryptjs (10 rounds), rate limiting (5 tentativas de login/15min, 50 requisições gerais/15min), CORS habilitado.
- **Arquitetura em camadas**: controllers, services, repositories e interfaces (`IUserRepository`), separando regras de negócio de acesso a dados.
- **Testes automatizados** com Jest (`controller.auth.spec.js`, `controller.users.spec.js`).
- **Stack**: Express.js 5, Node.js (ES Modules), MongoDB + Mongoose, Socket.io, JWT, bcryptjs, express-validator, express-rate-limit, Jest.

### ♟️ [chess_ai](https://github.com/mayconct32/chess_ai)
Assistente de xadrez em **Python + LangChain**, com pipeline de RAG (Retrieval-Augmented Generation): um PDF sobre xadrez é dividido em chunks (`langchain-text-splitters`, `pypdf`) e indexado num banco vetorial Chroma via `langchain-chroma`, com embeddings gerados por `fastembed`. Se a mensagem contiver notação **FEN**, a lib `chess` (python-chess) valida a posição e um motor externo (Stockfish) faz a análise. A resposta final é gerada via `langchain-google-genai` (Gemini). Interface via CLI; GUI planejada. Stack: Python 3.13, Poetry, LangChain (community, text-splitters, chroma, google-genai), fastembed, pypdf, python-chess.

### 📮 [correios_api](https://github.com/mayconct32/correios_api) — `correios-cep`
API em Python + FastAPI para consulta de CEP, consumindo a API pública dos **Correios** via `httpx` (cliente HTTP assíncrono) e persistindo dados em MySQL. Testes assíncronos com `pytest-asyncio` e `asgi-lifespan`. Projeto focado em integração com serviço externo de terceiros, fora do padrão CRUD comum dos outros repositórios.

### 🎙️ [ai_assistant](https://github.com/mayconct32/ai_assistant)
Assistente de voz em **Português** com **interface gráfica** (CustomTkinter), que ouve o microfone via `SpeechRecognition` + `PyAudio`, reconhece comandos por palavra de ativação ("chat") e executa ações simples (abrir sites, pesquisar), usando um modelo local via **Ollama**. Empacotável como executável standalone com PyInstaller. Projeto mais recente do portfólio (em desenvolvimento ativo). Stack: Python 3.13, Poetry, CustomTkinter, SpeechRecognition, PyAudio, Ollama, PyInstaller.

### 📖 [madr](https://github.com/mayconct32/madr) — MADR FastAPI
**Trabalho de Conclusão de Curso (TCC)**, do curso de FastAPI ministrado por Eduardo Mendes: "Meu Acervo Digital de Romances", uma API para gerenciar acervo de livros, usuários e autores (CRUD completo). É o projeto com a stack de dados mais robusta do portfólio: **SQLAlchemy assíncrono + Alembic** (migrations) sobre **PostgreSQL** (`psycopg`, `asyncpg`, com suporte a autenticação Kerberos via `gssapi`). Testes com `pytest-cov`, **Testcontainers** (banco real containerizado em teste) e **factory-boy** (fixtures de dados). Automação de tarefas via `taskipy`, formatação com Black + Ruff, execução via Docker Compose. Marca o início da minha trajetória com FastAPI antes dos projetos mais recentes.


### 🧮 [livro_entendendo_algoritmos](https://github.com/mayconct32/livro_entendendo_algoritmos)
Resumo do livro **"Entendendo Algoritmos"**, com resoluções de exercícios organizadas por capítulo (recursão, quicksort, tabelas hash, BFS, Dijkstra, algoritmos gulosos, programação dinâmica, KNN).

---

## 🏆 Achievements

🦈 Pull Shark x2
