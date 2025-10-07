# CausalQuant

> Graph-based financial data analysis platform leveraging Graph Neural Networks to uncover causal relationships between world events and market movements.

[![Python](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)](https://pytorch.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Overview

CausalQuant is a portfolio project demonstrating production-grade ML engineering practices, combining:

- **Knowledge Graphs**: Structured representation of financial entities and world events
- **Graph Neural Networks**: Deep learning on graph structures using PyTorch Geometric
- **Causal Inference**: Reasoning about cause-effect relationships in market movements
- **MLOps**: End-to-end model lifecycle management
- **DevOps**: Containerized, reproducible deployments

## Vision

Inspect causal relations between world events (geopolitical changes, economic indicators, corporate actions) and market movements by:

1. Constructing knowledge graphs from structured/unstructured financial data
2. Applying GNN-based causal inference models
3. Providing explainable, confidence-scored insights

## MoSCoW Requirements

### Must Have ✅
- Entity relation extraction from financial data & world business news
- Graph construction from structured and unstructured data
- Causal inference/reasoning module
- User-defined causal queries/metrics
- Model explainability interface
- Risk analysis

### Should Have 🎯
- Interactive dashboards for results exploration
- Automatic anomaly detection
- Backtesting/validation tools
- Add your own RSS feed

### Could Have 💡
- Simulate the impact of world events using Natural Language
- Exportable summaries (reports, CSV)
- Exploratory scraper using knowledge gap analysis
- API for plug-in to other quant platforms

### Won't Have ⛔
- Be an algorithmic trading program
- Proprietary black-box ML models
- Automated personal investment advice

## Architecture Principles

This project adheres to the [CausalQuant Constitution](.specify/memory/constitution.md) ensuring:

1. **Graph-First Architecture**: All data modeling centers on graph structures
2. **Test-Driven Development**: Mandatory TDD for all production code
3. **MLOps Pipeline Integration**: Versioned, tracked, reproducible ML models
4. **Containerization**: Docker-based deployment with orchestration
5. **Modular Library Architecture**: Independently testable, composable modules
6. **Data Quality & Observability**: Validation, logging, metrics throughout
7. **API-First Integration**: Abstracted external dependencies with versioned contracts
8. **Security & Compliance**: Secret management, dependency scanning, privacy awareness

## Technology Stack

- **Language**: Python 3.11+
- **Graph Framework**: PyTorch Geometric
- **ML Framework**: PyTorch 2.0+
- **Graph Storage**: Neo4j / NetworkX
- **API Framework**: FastAPI
- **Testing**: pytest (80%+ coverage)
- **MLOps**: MLflow
- **CI/CD**: GitHub Actions
- **Containerization**: Docker + Docker Compose

## Project Status

🚧 **In Development** - Initial setup and architecture definition phase.

This is a portfolio project built with best practices in:
- Software architecture
- Test-driven development
- MLOps practices
- Containerization & DevOps
- Production-grade ML engineering

## Getting Started

> Coming soon: Setup instructions, quickstart guide, and example notebooks.

## Development Workflow

1. **Feature Specification**: Define requirements, user stories, success criteria
2. **Planning**: Technical design, architecture decisions, constitution compliance
3. **Test-First**: Write tests before implementation
4. **Implementation**: Make tests pass
5. **Review**: Code review, security scan, quality gates
6. **Deploy**: Containerized deployment with CI/CD

See [Development Guidelines](.specify/templates/) for details.

## Contributing

This is a portfolio project, but feedback and suggestions are welcome! Please:
1. Review the [Constitution](.specify/memory/constitution.md)
2. Check existing issues/specs
3. Open an issue for discussion before submitting PRs

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Contact

**Daren Palmer**  
Portfolio Project - CausalQuant

---

*Built to demonstrate professional-grade ML engineering, software architecture, and DevOps practices.*

