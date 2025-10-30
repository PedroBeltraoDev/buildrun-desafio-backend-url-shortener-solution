# 🔗 URL Shortener (Encurtador de URL) - Build & Run Challenge Solution

[![Java](https://img.shields.io/badge/Java-21-399b1e?style=for-the-badge&logo=java&logoColor=white)](https://www.java.com/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.1-6DB33F?style=for-the-badge&logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)

## 📝 Sobre o Projeto

Este projeto é um serviço backend de **Encurtamento de URL**, desenvolvido como solução para um desafio da **Build & Run**. Ele permite encurtar links longos e gerencia o redirecionamento para o endereço original.

### Tecnologias Principais
* **Backend:** Spring Boot 3 (Java 21)
* **Banco de Dados:** MongoDB (com índice TTL para expiração automática de links)
* **Containerização:** Docker Compose

## ✨ Funcionalidades

* **Encurtamento Rápido:** Recebe uma URL longa e gera um ID alfanumérico (5-10 caracteres).
* **Redirecionamento:** O endpoint `GET /{id}` realiza o redirecionamento HTTP (`302 Found`) para a URL original.
* **Expiração Automática:** Links expiram e são removidos do MongoDB automaticamente após um tempo de validade definido.
* **Tratamento de Erros:** Retorna `404 Not Found` para links inválidos ou expirados.

## ⚙️ Como Executar

### 1. Inicializar o Banco de Dados
Use o Docker Compose para subir o container do MongoDB:

```bash
docker compose up -d
