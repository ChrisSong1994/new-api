<div align="center">

# AI Gateway

**Enterprise AI API Gateway and Management Platform**

<p align="center">
  <a href="./README.zh_CN.md">简体中文</a> | <strong>English</strong>
</p>

</div>

## Overview

AI Gateway is a unified API gateway for large language models (LLMs) that aggregates multiple upstream AI providers behind a standardized interface. It provides user management, billing, rate limiting, and an admin dashboard.

## Quick Start

### Docker Compose (Recommended)

```bash
# Clone the project
git clone <your-repo-url>
cd my-new-api

# Start the service
docker-compose up -d
```

### Docker Command

```bash
# Using SQLite (default)
docker run --name ai-gateway -d --restart always \
  -p 3000:3000 \
  -e TZ=Asia/Shanghai \
  -v ./data:/data \
  <your-image>:latest
```

After deployment, visit `http://localhost:3000` to get started.

## Key Features

### Core Functions

- Modern UI design
- Multi-language support (Chinese, English)
- Data visualization dashboard
- Token grouping and model restrictions
- User management

### Payment and Billing

- Online recharge (EPay, Stripe)
- Pay-per-use pricing
- Flexible billing policy configuration

### Authorization and Security

- OAuth login (GitHub, Discord, OIDC)
- WebAuthn/Passkeys support
- Token quota management

### API Support

- OpenAI Compatible API
- Claude Messages
- Google Gemini
- Rerank Models (Cohere, Jina)

## Deployment

### Requirements

| Component | Requirement |
|------|------|
| Local database | SQLite |
| Remote database | MySQL ≥ 5.7.8 or PostgreSQL ≥ 9.6 |
| Container engine | Docker / Docker Compose |

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `SESSION_SECRET` | Session secret (required for multi-instance) | - |
| `CRYPTO_SECRET` | Encryption secret (required for Redis) | - |
| `SQL_DSN` | Database connection string | - |
| `REDIS_CONN_STRING` | Redis connection string | - |
| `STREAMING_TIMEOUT` | Streaming timeout (seconds) | `300` |

## License

This project is licensed under a commercial license. All rights reserved.