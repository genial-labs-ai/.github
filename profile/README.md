# Genial Labs

We build and teach **evaluation-driven AI agents**: the harness, the tests and the CI gate around a
model matter as much as the model itself.

## Workshops

| | |
|---|---|
| [**Evaluating Autonomous Agents: Systems, Harnesses & AWS Production CI/CD**](https://github.com/genial-labs-ai/system_agent_harness_aws) | Four days, one running example (*Stockroom*, an inventory agent with seeded weaknesses). Deterministic metrics, calibrated LLM judges, OpenTelemetry traces, a custom harness with MCP tools, red-teaming, and a GitHub Actions gate that runs offline by default and on Amazon Bedrock through OIDC when asked. |

[![agent-eval-ci](https://github.com/genial-labs-ai/system_agent_harness_aws/actions/workflows/agent_eval_ci.yml/badge.svg)](https://github.com/genial-labs-ai/system_agent_harness_aws/actions/workflows/agent_eval_ci.yml)

## How we work

- **Offline-first.** Every lab and every test runs with no cloud credentials; live cloud is opt-in.
- **No fabricated facts.** Figures in teaching materials are reproduced from the repo; post-mortems are labelled composite or linked to a source.
- **Agent = Model + Harness.** Every claim about a failure mode is demonstrated by a test or a notebook cell.

[genial-labs.com](https://genial-labs.com)
