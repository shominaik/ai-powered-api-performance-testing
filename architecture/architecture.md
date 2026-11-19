# High-Level Architecture

## Current Proof-of-Concept Flow

```text
Engineer
   |
   v
Codex CLI (AI agent)
   |
   | MCP tool calls
   v
Feather Wand MCP Server
   |
   | JMeter plan inspection / editing / execution
   v
Apache JMeter
   |
   | HTTP requests
   v
Sample FastAPI application
```

## Component Responsibilities

- **Engineer:** Defines the test objective, reviews proposed changes, and approves execution.
- **Codex CLI:** Interprets instructions, reasons about the test plan, and coordinates tool calls.
- **Feather Wand MCP Server:** Exposes supported JMeter operations to the agent through MCP.
- **Apache JMeter:** Stores, configures, and executes the performance test plan.
- **FastAPI sample application:** Provides a controlled API workflow for the proof of concept.

## Intended Future Direction

The longer-term concept is to separate responsibilities into specialised agents:

- Test Plan Agent — prepares or analyses test plans.
- Correlation Agent — identifies dynamic values and configures extractors.
- Performance Agent — configures workload and executes approved tests.
- Analysis Agent — interprets results and prepares reports.

Microsoft Foundry is a candidate orchestration platform for this future multi-agent design. This is a roadmap concept, not a capability delivered by the current POC.

## Important Boundaries

AI-proposed changes must be reviewed. Probe and load-test execution can affect the target system; use only authorised test environments and controlled workloads. Never expose MCP bearer tokens, API credentials, or personal data in source control.
