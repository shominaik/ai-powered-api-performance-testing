# AI-Powered API Performance Testing Framework

An AI-assisted framework for analysing API workflows, identifying dynamic values, configuring Apache JMeter correlation, and validating performance tests through agent-assisted workflows.

## Vision

Move API performance testing from a largely manual workflow toward an AI-assisted process that can analyse recorded traffic, prepare JMeter test plans, identify correlation requirements, execute tests, and summarise results.

## Proof of Concept

The current proof of concept uses a sample Riga Shop API workflow to demonstrate dynamic-value correlation across multiple dependent API requests.

**Current status:** Proof of Concept — In Progress. This repository does not claim a production-ready or fully autonomous correlation solution.

## Technology Stack

- Apache JMeter 5.6.3
- Feather Wand 4.0
- Codex CLI
- Model Context Protocol (MCP)
- FastAPI
- Microsoft Foundry — planned future orchestration layer

## High-Level Workflow

1. Prepare or record an API workflow.
2. Inspect the JMeter test plan and identify dynamic values.
3. Configure extractors and replace hard-coded values with variables.
4. Execute the test and validate the end-to-end workflow.
5. Review performance results and refine the test.

See [`architecture/architecture.md`](architecture/architecture.md).

## Repository Structure

```text
.
├── README.md
├── .gitignore
├── architecture/
├── docs/
├── examples/
├── poc/
└── screenshots/
```

## Roadmap

### Phase 1 — Proof of Concept
- Demonstrate a multi-request API workflow in JMeter.
- Explore AI-assisted correlation analysis using Feather Wand and Codex CLI.
- Validate extracted values against downstream requests.

### Phase 2 — Workflow Automation
- Automate test-plan inspection and correlation configuration.
- Add repeatable validation and execution workflows.
- Improve result analysis and reporting.

### Phase 3 — Multi-Agent Architecture
- Introduce specialised agents for test-plan generation, correlation, execution, and analysis.
- Evaluate Microsoft Foundry for agent orchestration.

## Security

Never commit API keys, bearer tokens, passwords, session identifiers, local Codex configuration, generated test results, or machine-specific settings. Review every JMX, properties file, HAR file, and script before publishing.

## Disclaimer

This is an experimental proof of concept. Validate all generated test plans and correlation changes before using them against non-test systems.

## Development Log

- Initial GitHub repository created.
- Initial project structure published.
- Git workflow configured successfully.

 ## Git Learning

- Practised Git initialisation.
- Practised committing and pushing changes.
- Learning to pull remote changes.
