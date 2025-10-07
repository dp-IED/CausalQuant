<!--
SYNC IMPACT REPORT
==================
Version Change: 0.0.0 → 1.0.0
Modified Principles: N/A (initial constitution)
Added Sections:
  - Core Principles (8 principles)
  - Architecture Standards
  - Development Workflow
  - Governance
Removed Sections: N/A
Templates Status:
  ✅ plan-template.md - reviewed, Constitution Check section ready
  ✅ spec-template.md - reviewed, requirements alignment verified
  ✅ tasks-template.md - reviewed, task categorization aligns with principles
Follow-up TODOs: None
Rationale: MAJOR version 1.0.0 as this is the initial ratification establishing all core principles and governance.
-->

# CausalQuant Constitution

## Core Principles

### I. Graph-First Architecture

All data modeling MUST center on graph structures representing entities and relationships. Graph Neural Networks (GNNs) using PyTorch Geometric are the primary analytical tools. Non-graph data sources MUST be transformed into graph representations (nodes, edges, features) before analysis. Every feature MUST justify its place in the knowledge graph paradigm.

**Rationale**: The project's core value proposition is uncovering causal relationships between world events and market movements through graph-based reasoning. This requires consistent graph-native thinking.

### II. Test-Driven Development (NON-NEGOTIABLE)

TDD is mandatory for all production code. Sequence: write tests → get user/spec approval → verify tests fail → implement → verify tests pass → refactor. Red-Green-Refactor cycle strictly enforced. No implementation code merged without corresponding tests.

**Rationale**: Portfolio project excellence demands demonstrable code quality. TDD ensures correctness, facilitates refactoring, and serves as living documentation for recruiters/stakeholders.

### III. MLOps Pipeline Integration

All ML models MUST be versioned, tracked, and reproducible. Model training, evaluation, and deployment MUST be automated through MLOps pipelines. Experiment tracking (metrics, hyperparameters, artifacts) is mandatory. Models MUST include versioned schemas for input/output contracts.

**Rationale**: Production-grade ML systems require reproducibility, auditability, and automated deployment. This demonstrates professional-level ML engineering beyond notebook prototypes.

### IV. Containerization & Orchestration

All services MUST be containerized using Docker with multi-stage builds for optimization. Docker Compose MUST be used for local development orchestration. Production-ready Dockerfiles MUST minimize attack surface (non-root users, minimal base images, security scanning).

**Rationale**: Modern deployment practices require containerization for consistency across environments. Portfolio projects MUST demonstrate DevOps competency.

### V. Modular Library Architecture

Core functionality MUST be organized as independently testable libraries/modules. Each module MUST have clear boundaries, documented interfaces, and single responsibility. Modules MUST be reusable and composable. Avoid monolithic code blocks.

**Rationale**: Professional software engineering demands modularity for maintainability, testing, and scalability. Recruiters assess architectural thinking through code organization.

### VI. Data Quality & Observability

All data pipelines MUST include validation, error handling, and logging. Financial data ingestion MUST verify data integrity (schema validation, null checks, range validation). System MUST expose health metrics and operational telemetry. Causal inference results MUST include confidence scores and uncertainty quantification.

**Rationale**: Financial analysis depends on data quality. Observability enables debugging and builds trust in causal conclusions. Production systems must be monitorable.

### VII. API-First Integration

External data sources (financial APIs, news feeds) MUST be abstracted behind service interfaces. API clients MUST handle rate limiting, retries, and error cases gracefully. Contracts (schemas, endpoints) MUST be versioned and documented. Mock implementations MUST exist for testing.

**Rationale**: Decoupling data acquisition from analysis logic enables testing, swapping providers, and managing API evolution. Professional systems isolate external dependencies.

### VIII. Security & Compliance Awareness

Secrets (API keys, credentials) MUST NEVER be committed to version control. Use environment variables or secret management tools. Financial data handling MUST consider privacy implications. Dependencies MUST be scanned for known vulnerabilities. Authentication/authorization MUST be implemented for any exposed APIs.

**Rationale**: Financial data systems have security obligations. Portfolio projects must demonstrate security awareness to meet professional standards.

## Architecture Standards

### Technology Stack

- **Language**: Python 3.11+
- **Graph Library**: PyTorch Geometric (torch-geometric)
- **ML Framework**: PyTorch 2.0+
- **Graph Storage**: Neo4j or NetworkX (for development/small graphs)
- **API Framework**: FastAPI for REST APIs
- **Testing**: pytest with coverage reporting (minimum 80% coverage)
- **MLOps**: MLflow for experiment tracking, model registry
- **CI/CD**: GitHub Actions or GitLab CI
- **Containerization**: Docker with Docker Compose

### Code Quality Gates

All pull requests MUST pass:
- Linting (pylint, flake8, or ruff)
- Type checking (mypy with strict mode)
- Unit tests (80%+ coverage)
- Integration tests for API endpoints
- Security scanning (bandit, safety)
- Dockerfile best practice checks (hadolint)

### Performance Standards

- API endpoints: <500ms p95 response time for queries
- Graph construction: handle minimum 10,000 nodes efficiently
- Model inference: <2 seconds for single prediction
- Memory: <4GB for baseline models (scalability via config)

### Documentation Requirements

Each module MUST include:
- Docstrings (Google or NumPy style) for all public functions/classes
- Type hints for all function signatures
- README with quickstart example
- API documentation (auto-generated from OpenAPI specs)

Models MUST include:
- Model card documenting purpose, training data, performance metrics
- Versioned schemas for input/output
- Example usage notebook

## Development Workflow

### Feature Development Process

1. **Specification**: Create feature spec with user stories, requirements, success criteria
2. **Planning**: Generate implementation plan with technical context, structure, constitution compliance check
3. **Research**: Document technical approach, library selection, design decisions
4. **Test Definition**: Write tests first (contract tests, integration tests, unit tests)
5. **Implementation**: Implement to make tests pass
6. **Review**: Code review checking tests, architecture, security
7. **Integration**: Merge to main with CI/CD validation
8. **Deployment**: Containerized deployment with rollback capability

### Git Workflow

- Feature branches: `###-feature-name` format
- Commits: Conventional Commits format (feat:, fix:, docs:, test:, refactor:, chore:)
- PRs: Must reference issue/spec, include test evidence, pass all CI checks
- Main branch: Protected, always deployable
- Tags: Semantic versioning for releases (v1.2.3)

### Testing Strategy

- **Unit Tests**: Isolated tests for individual functions/classes (mocked dependencies)
- **Integration Tests**: Multi-component tests (API + service + database)
- **Contract Tests**: API endpoint contracts (request/response schemas)
- **Model Tests**: Validation tests (known inputs → expected outputs), performance benchmarks
- **E2E Tests**: Full pipeline tests (data ingestion → graph construction → model inference)

### Code Review Checklist

- [ ] Constitution compliance verified
- [ ] Tests written first and pass
- [ ] Type hints present
- [ ] Docstrings complete
- [ ] No secrets in code
- [ ] Error handling comprehensive
- [ ] Logging appropriate
- [ ] Performance acceptable
- [ ] Security scan passed
- [ ] Docker build succeeds

## Governance

### Amendment Process

This constitution supersedes all other practices. Amendments require:
1. Documented rationale for change
2. Impact assessment on existing code/templates
3. Version bump per semantic versioning rules
4. Update to all dependent templates (.specify/templates/)
5. Sync Impact Report prepended to constitution file

### Versioning Policy

- **MAJOR**: Backward incompatible governance changes or principle removals
- **MINOR**: New principles added or material expansions
- **PATCH**: Clarifications, wording fixes, non-semantic refinements

### Compliance Review

All PRs MUST verify compliance with this constitution. Violations MUST be:
- Documented in Complexity Tracking section of plan.md
- Justified with "Why Needed" explanation
- Include "Simpler Alternative Rejected Because" analysis

Complexity/violations without justification will be rejected in code review.

### Runtime Development Guidance

For day-to-day development guidance beyond this constitution, refer to project documentation:
- `/specs/` directory for feature specifications
- `plan.md` files for implementation plans
- `quickstart.md` files for setup instructions
- Model cards for ML model usage

**Version**: 1.0.0 | **Ratified**: 2025-10-07 | **Last Amended**: 2025-10-07
