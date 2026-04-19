<div align="center">

# SovereignQuant

### Institutional-Grade Crypto Futures Trading Infrastructure

**Monte Carlo Risk Assessment | Market Regime Detection | Algorithmic Execution**

[![License: Commercial](https://img.shields.io/badge/License-Commercial-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.11+-3776AB.svg)](https://python.org)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED.svg)](https://docker.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-TimescaleDB-336791.svg)](https://timescale.com)

</div>

---

> "The power to create wealth through code is the ultimate expression of individual sovereignty in the digital age."

---

## Executive Summary

SovereignQuant is a production-ready trading infrastructure designed for quantitative developers and institutional operators who require autonomy, security, and performance without compromise. This is not a toy, nor a backtest-only simulator. It is a complete operational framework for deploying sophisticated algorithmic strategies on Binance Futures with institutional-grade risk controls.

### The Sovereign Philosophy

Financial sovereignty is a fundamental right. In an era of centralized control, surveillance, and arbitrary restrictions, the ability to programmatically manage capital without intermediaries represents the pinnacle of individual empowerment.

- **No Platform Lock-in**: Your code. Your servers. Your keys.
- **Radical Transparency**: Every trade, every calculation, every risk metric is auditable.
- **Complete Autonomy**: Deploy on a home server, a VPS in any jurisdiction, or a distributed cluster.
- **Zero Trust Architecture**: Cryptographic security, encrypted API keys, kill-switches, and circuit breakers.

---

## Core Capabilities

### 1. Binance Futures Integration

Unified margin mode support with real-time WebSocket market data feeds. Features sub-account isolation, seamless testnet-to-live transition, and comprehensive position and order management capabilities.

### 2. Monte Carlo Risk Simulations

Stochastic modeling infrastructure executing 10,000+ simulation runs per strategy evaluation. Calculates Value-at-Risk (VaR) and Conditional VaR, generates drawdown probability distributions, optimizes position sizing, and provides black swan scenario stress testing.

### 3. Market Regime Detection

Four-state classification system (Low/Normal/High/Crisis volatility regimes) with trend strength measurement via ADX-based algorithms. Detects correlation breakdowns, enables dynamic strategy selection based on detected regime, and provides regime transition probability forecasting.

### 4. Risk Management Layer

Configurable kill switches with drawdown thresholds, maximum drawdown circuit breakers, position size limits with portfolio heat monitoring, correlation-adjusted exposure limits, and automated equity curve monitoring.

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────────────────┐
│                              PRESENTATION                                │
│  ┌─────────────┐  React 19 + TypeScript + Tailwind CSS + Framer Motion  │
│  │   Next.js   │  Real-time WebSocket charts, Dark-first UI            │
│  │   :3000     │  Progressive Web App capable                          │
│  └──────┬──────┘                                                        │
├─────────┼───────────────────────────────────────────────────────────────┤
│         │                           API LAYER                           │
│  ┌──────▼──────┐  FastAPI + Pydantic + SQLAlchemy 2.0                  │
│  │   Backend   │  Async/await throughout, automatic OpenAPI docs        │
│  │   :8000     │  JWT authentication, rate limiting, request logging  │
│  └──────┬──────┘                                                        │
├─────────┼───────────────────────────────────────────────────────────────┤
│         │                          SERVICES                             │
│  ┌──────▼──────┐  ┌──────────────┐  ┌──────────────┐                    │
│  │   Worker    │  │   Monitor    │  │   Redis      │                    │
│  │  Process    │  │   Service    │  │   Cache      │                    │
│  │  Optimization│  │  Execution   │  │  Pub/Sub     │                    │
│  └──────┬──────┘  └──────┬───────┘  └──────┬───────┘                    │
├─────────┼────────────────┼────────────────┼─────────────────────────────┤
│         │                │                │                           │
│  ┌──────▼──────┐  ┌──────▼──────┐  ┌──────▼──────┐                    │
│  │ TimescaleDB │  │  Binance    │  │  Notification│                    │
│  │  PostgreSQL │  │    API      │  │   Services   │                    │
│  └─────────────┘  └─────────────┘  └─────────────┘                    │
└─────────────────────────────────────────────────────────────────────────┘
```

### Technology Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | Next.js 15, React 19, TypeScript, Tailwind CSS v4, Recharts |
| **Backend API** | FastAPI, Uvicorn, Pydantic v2, SQLAlchemy 2.0 |
| **Data Science** | Pandas 2.0+, NumPy 1.24+, CCXT Pro |
| **Database** | PostgreSQL 15 + TimescaleDB (time-series optimized) |
| **Cache/Queue** | Redis 7 (caching, pub/sub, Celery broker) |
| **Deployment** | Docker, Docker Compose, Nginx |
| **Security** | Cryptography (Fernet), JWT, encrypted at-rest |

---

## Quick Start Guide

### Prerequisites

- **Docker** 24.0+ and Docker Compose 2.20+
- **Git** (for cloning)
- **4GB+ RAM** (8GB recommended for production)
- **Binance Account** with Futures enabled (start with Testnet)

### 1. Clone and Configure

```bash
# Clone the repository
git clone https://github.com/yourusername/sovereign-quant-boilerplate.git
cd sovereign-quant-boilerplate

# Copy the environment template
cp .env.example .env

# Edit .env with your configuration
nano .env  # or use your preferred editor
```

### 2. Generate Security Keys

```bash
# Generate encryption key for API credentials
openssl rand -hex 32

# Copy this value to ENCRYPTION_KEY in your .env

# Generate JWT secret
openssl rand -base64 32

# Copy to JWT_SECRET_KEY in your .env
```

### 3. Configure Binance (Testnet First)

1. Visit [Binance Futures Testnet](https://testnet.binancefuture.com/)
2. Generate API Key and Secret
3. Add to `.env`:
   ```
   BINANCE_API_KEY=your_testnet_key
   BINANCE_API_SECRET=your_testnet_secret
   USE_TESTNET=true
   ```

### 4. Launch Infrastructure

```bash
# Build and start all services
docker-compose up -d

# Verify all services are healthy
docker-compose ps

# View logs
docker-compose logs -f backend
docker-compose logs -f worker
```

### 5. Access the Platform

| Service | URL | Description |
|---------|-----|-------------|
| Dashboard | http://localhost:3000 | Trading interface |
| API Docs | http://localhost:8000/docs | Interactive OpenAPI/Swagger |
| API (Alt) | http://localhost:8000/redoc | ReDoc documentation |
| Database | localhost:5432 | TimescaleDB |
| Redis | localhost:6379 | Cache/Queue |

### 6. Initialize Database

```bash
# Run migrations (inside backend container)
docker-compose exec backend alembic upgrade head

# Or manually create tables on first run
# (automatic on startup if configured)
```

### 7. Verify Trading (Testnet)

```bash
# Check exchange connectivity
curl http://localhost:8000/api/v1/exchange/status

# View account balance
curl http://localhost:8000/api/v1/account/balance \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"

# Start paper trading
curl -X POST http://localhost:8000/api/v1/trading/mode \
  -H "Content-Type: application/json" \
  -d '{"mode": "paper", "symbol": "BTCUSDT"}'
```

---

## Directory Structure

```
sovereign-quant-boilerplate/
├── backend/                    # FastAPI application
│   ├── api/                   # Route handlers
│   ├── core/                  # Config, security, logging
│   ├── models/                # SQLAlchemy ORM
│   ├── schemas/               # Pydantic models
│   ├── services/              # Business logic
│   │   ├── binance_service.py
│   │   ├── risk_controller.py
│   │   ├── regime_detector.py
│   │   └── monte_carlo.py
│   └── main.py                # Application entry
├── frontend/                   # Next.js application
│   ├── src/
│   │   ├── app/              # App router (Next.js 13+)
│   │   ├── components/       # React components
│   │   ├── hooks/            # Custom React hooks
│   │   ├── lib/              # Utilities
│   │   └── types/            # TypeScript definitions
│   ├── public/               # Static assets
│   └── package.json
├── worker/                     # Background processing
│   ├── optimization_engine.py
│   ├── signal_processor.py
│   └── trade_executor.py
├── database/                   # Migrations & schemas
│   ├── init/
│   └── migrations/
├── monitoring/                 # Prometheus/Grafana
│   ├── prometheus.yml
│   └── grafana/
├── nginx/                      # Reverse proxy config
├── docker-compose.yml          # Production orchestration
├── Dockerfile                  # Multi-stage build
└── .env.example               # Configuration template
```

---

## Configuration Reference

### Critical Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `BINANCE_API_KEY` | Required | Exchange API key |
| `BINANCE_API_SECRET` | Required | Exchange API secret |
| `USE_TESTNET` | Required | `true` for testnet, `false` for live |
| `ENCRYPTION_KEY` | Required | 64-char hex for credential encryption |
| `JWT_SECRET_KEY` | Required | Session signing key |
| `DATABASE_URL` | Required | PostgreSQL connection string |
| `REDIS_URL` | Required | Redis connection string |
| `ENABLE_LIVE_TRADING` | Required | `false` until explicitly ready |
| `ADMIN_PASSWORD` | Required | Change from default immediately |

### Risk Control Settings

```env
# Position Limits
MAX_POSITION_SIZE_USD=1000
MAX_LEVERAGE=5
MAX_OPEN_POSITIONS=3

# Risk Per Trade
RISK_PER_TRADE_PERCENT=2.0
MAX_DAILY_LOSS_PERCENT=5.0
MAX_WEEKLY_LOSS_PERCENT=10.0

# Kill Switch (emergency shutdown)
ENABLE_KILL_SWITCH=true
KILL_SWITCH_THRESHOLD=0.15  # 15% drawdown triggers halt
```

### Monte Carlo Settings

```env
MC_SIMULATION_RUNS=10000
MC_CONFIDENCE_LEVEL=0.95
MC_USE_ANTITHETIC_VARIATES=true
MC_BLACK_SWAN_PROBABILITY=0.01
```

---

## Risk Management Features

### Kill Switch System

The kill switch is a non-negotiable safety mechanism that:
- Monitors account equity in real-time
- Immediately cancels all open orders on threshold breach
- Closes all positions (configurable: market or limit)
- Sends alerts via all configured channels
- Requires manual reset after activation

### Regime-Based Strategy Guardrails
- Prevents trend-following strategies in ranging markets
- Reduces position size in high volatility regimes
- Automatically selects mean-reversion in mean-reverting regimes
- Logs all regime transitions for audit

### Pre-Trade Risk Checks (Every Order)
1. Maximum position size not exceeded
2. Portfolio heat within limits
3. Correlation exposure acceptable
4. Sufficient margin buffer
5. No duplicate signal detection
6. Kill switch not activated

---

## Deployment Options

### Development (Local)
```bash
docker-compose up -d
```

### Production VPS (Single Node)
```bash
# Copy .env.production and configure
docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d
```

### With Monitoring Stack
```bash
docker-compose --profile monitoring up -d
# Access Grafana at http://localhost:3001 (admin/admin)
```

### Cloud Providers
- **AWS**: Use ECS or EKS with RDS PostgreSQL and ElastiCache
- **GCP**: Cloud Run for API, Cloud SQL, Memorystore
- **DigitalOcean**: Managed PostgreSQL + Redis, Docker Droplet
- **Hetzner**: Cost-effective dedicated servers

---

## API Documentation

Interactive documentation is automatically generated:

- **Swagger UI**: http://localhost:8000/docs
- **ReDoc**: http://localhost:8000/redoc
- **OpenAPI JSON**: http://localhost:8000/openapi.json

### Example API Call

```bash
# Authenticate and get token
TOKEN=$(curl -s -X POST http://localhost:8000/api/v1/auth/login \
  -H "Content-Type: application/json" \
  -d '{"username":"admin","password":"your_password"}' \
  | jq -r '.access_token')

# Fetch portfolio status
curl http://localhost:8000/api/v1/portfolio/status \
  -H "Authorization: Bearer $TOKEN" \
  | jq
```

---

## Licensing Tiers

SovereignQuant is available under two commercial license tiers:

### Sovereign (Personal) — $349

**For individual quantitative developers managing personal capital.**

Includes:
- Full source code access
- Single deployment license (personal use only)
- Self-managed fund operations
- Access to private GitHub repository
- Core infrastructure updates

Restrictions:
- Personal use only
- No commercial or SaaS deployment
- No resale or redistribution rights

---

### Enterprise (Commercial) — $899

**For prop firms, funds, and SaaS operators.**

Includes:
- Everything in Sovereign tier
- Commercial use license
- SaaS deployment rights
- Fund operation authorization
- Multiple deployment instances
- White-label rights available (contact for terms)
- Priority support queue

Target Users:
- Proprietary trading firms
- Crypto hedge funds
- Trading infrastructure SaaS providers
- Multi-account operators

---

## Support Policy

SovereignQuant is engineered for technically autonomous quantitative developers. Our support model reflects the product's self-reliant philosophy.

### Support Method

All support is handled **exclusively via GitHub Issues** in the private repository.

- **Response Time:** 48-72 hours (working days)
- **Support Scope:** Core infrastructure bugs and technical defects only
- **No Direct Messaging:** All communication is asynchronous through GitHub

### In Scope

- Infrastructure bugs and defects
- Installation and deployment issues
- API and integration problems
- Security vulnerabilities

### Explicitly Out of Scope

The following are **NOT** provided under any license tier:

- **Strategy Development:** No financial strategy consulting, backtest validation, or trading logic advisory.
- **Programming Tutoring:** No Python lessons, Docker training, or general software engineering instruction.
- **Custom Deployments:** No 1-on-1 setup calls, server configuration assistance, or infrastructure management services.
- **Financial Advice:** No investment recommendations, portfolio advice, or trading decisions guidance.

### Contact

For critical access issues or payment inquiries: **peeraphol.ka@gmail.com**

*(Note: This email is for billing and access issues only. Technical support must go through GitHub Issues.)*

---

## Documentation

Documentation is intentionally minimal. SovereignQuant is built on industry-standard technologies with extensive public documentation:

| Topic | Resource |
|-------|----------|
| **FastAPI** | https://fastapi.tiangolo.com |
| **Next.js** | https://nextjs.org/docs |
| **TimescaleDB** | https://docs.timescale.com |
| **SQLAlchemy** | https://docs.sqlalchemy.org |
| **CCXT** | https://docs.ccxt.com |

### API Reference

Once running, interactive documentation is available at:
- **Swagger UI:** http://localhost:8000/docs
- **ReDoc:** http://localhost:8000/redoc
- **OpenAPI JSON:** http://localhost:8000/openapi.json

---

## License & Legal

### Commercial License

This software is provided under a **Commercial License**. See [LICENSE](LICENSE) for full terms.

### STRICT FINANCIAL DISCLAIMER

**SOVEREIGNQUANT IS SOFTWARE, NOT FINANCIAL ADVICE.**

By using this software, you acknowledge and agree to the following:

1. **No Guarantees:** Past performance of any strategy or algorithm does not guarantee future results. Markets are inherently unpredictable.

2. **Risk of Loss:** Cryptocurrency futures trading involves **substantial risk of loss** and is not suitable for all investors. You may lose more than your initial investment.

3. **No Liability:** The authors, contributors, and distributors of SovereignQuant assume **no liability** for any trading losses, system failures, data inaccuracies, or damages arising from the use of this software.

4. **Your Responsibility:** You are solely responsible for:
   - Strategy development and validation
   - Risk parameter configuration
   - Capital allocation decisions
   - Compliance with local laws and regulations
   - Security of your API keys and infrastructure

5. **Not Investment Advice:** No communication from SovereignQuant or its representatives constitutes investment advice, recommendation, or solicitation.

6. **Sovereign Risk:** You operate this software at your own risk. The "sovereign" concept emphasizes **individual responsibility**. There is no safety net, no bailout, and no recourse for poor decisions.

7. **Test Thoroughly:** Always use testnet and paper trading extensively before deploying real capital.

**Use this software at your own risk. Trade responsibly. Protect your capital.**

---

## Contributing

While SovereignQuant is primarily a commercial product, we welcome:
- Bug reports via GitHub Issues
- Security vulnerability reports (see SECURITY.md)
- Feature requests for roadmap consideration

---

## Acknowledgments

SovereignQuant is built on the shoulders of open-source giants:
- [FastAPI](https://fastapi.tiangolo.com/) by Sebastián Ramírez
- [CCXT](https://github.com/ccxt/ccxt) by the CCXT team
- [TimescaleDB](https://www.timescale.com/) for time-series excellence
- [Next.js](https://nextjs.org/) by Vercel

---

<div align="center">

**[Back to Top](#sovereignquant)**

*Built for those who refuse to outsource their financial destiny.*

</div>
