# Secure Document Intelligence API

Document intelligence and Retrieval-Augmented Generation backend built with FastAPI, PostgreSQL and pgvector.

## Overview
The system processes documents, extracts and chunks text, generates embeddings, stores vectors in PostgreSQL/pgvector and retrieves relevant context for language-model responses.

## Existing Technologies
- Python / FastAPI
- PostgreSQL / pgvector
- SQLAlchemy
- OpenAI API / embeddings
- Pydantic
- Docker / Docker Compose
- pytest tooling

## Architecture
```text
Document -> Text Extraction -> Chunking -> Embeddings
          -> PostgreSQL + pgvector -> Retrieval -> Context -> LLM -> Response
```

## Currently Implemented
- PDF/document processing
- chunking and embeddings
- PostgreSQL/pgvector persistence and similarity retrieval
- RAG workflow and streaming responses
- connection pooling
- structured logging and error handling
- rate limiting
- CORS/security middleware and file validation
- Docker/Docker Compose and health checks

## Security
Currently demonstrated/documented: environment-based configuration, rate limiting, validation, CORS controls, security headers and SQLAlchemy access. JWT authentication and RBAC are not claimed as existing features.

## Testing
```bash
pytest
pytest --cov=app --cov-report=html
```

## Docker
```bash
cp .env.example .env
docker-compose up --build
```
Never commit a real `.env`.

## Planned Portfolio Enhancements
- JWT registration/login
- RBAC and per-user document ownership
- document-level authorization
- prompt-injection protection
- retrieval evaluation and citation validation
- semantic caching and PII protection
- additional security tests
