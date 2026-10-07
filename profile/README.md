# Genial Labs

Machine learning workshops taught from working code. You clone the repository and run the labs; the
slides are there to explain what you just saw.

The bias throughout is towards evaluation. A model is the easy half of a system. The other half —
the harness that calls it, the tests that hold it to account, the gate that stops a regression
reaching production — is where the failures live, so that is where the labs spend their time.

## Workshops

### [Evaluating Autonomous Agents: Systems, Harnesses & AWS Production CI/CD](https://github.com/genial-labs-ai/system_agent_harness_aws)

**Four days.** [Workshop site](https://genial-labs-ai.github.io/system_agent_harness_aws/) ·
[![agent-eval-ci](https://github.com/genial-labs-ai/system_agent_harness_aws/actions/workflows/agent_eval_ci.yml/badge.svg)](https://github.com/genial-labs-ai/system_agent_harness_aws/actions/workflows/agent_eval_ci.yml)

One running example: *Stockroom*, an inventory and order-support agent with five tools, a 50-case
golden set, and four deliberately seeded weaknesses — an ambiguous tool description, an oversized
tool payload, an unbounded retry, an unguarded prompt injection. Each is a feature flag, so you
switch it on, measure what it costs, then fix it in the harness. The ambiguous description alone
drops tool-selection accuracy from 1.00 to 0.64 in the deterministic mock run while answers
can still look right, which is the point of the workshop.

Along the way: deterministic trajectory metrics, LLM judges calibrated against 32 human-labelled
cases and probed for position, verbosity and self-preference bias, OpenTelemetry traces, tools
served over MCP, a red-team suite, and a GitHub Actions gate that fails the pull request when a
metric slips against the committed baseline. All of it runs offline against a deterministic fake
model and fake judge, so no cloud account is needed. Amazon Bedrock is opt-in; live CI uses
GitHub OIDC with no long-lived keys. A live run caps its own tokens, steps and wall-clock time,
and reports what it used.

### [From Traditional NLP to Modern LLMs](https://github.com/genial-labs-ai/nlp-llms)

**Five days.** [Workshop site](https://genial-labs-ai.github.io/nlp-llms/) ·
[Schedule](https://genial-labs-ai.github.io/nlp-llms/schedule.html)

Fifteen modules from n-grams to agents: text as data, word vectors, sequence models, attention, a
transformer written from scratch, pretraining on the Hugging Face stack, LoRA fine-tuning,
preference learning and RLHF, calibration, retrieval-augmented generation, and a capstone that
fills most of the last day in pairs. Modules 1–14 pair a short lecture with a Colab notebook;
Module 15 is the hands-on capstone. API keys are optional: labs provide free open-model paths
or, for calibrated decisions, a small decision model trained in the lab.

Still being hardened for the Colab runtime — the
[readiness page](https://genial-labs-ai.github.io/nlp-llms/readiness.html) states exactly which labs
have run end to end and where. Development happens at
[project-delphi/nlp-llms](https://github.com/project-delphi/nlp-llms); the copy here is a mirror.

### [Tensors for Machine Learning](https://github.com/genial-labs-ai/tensors-workshop)

**One day.** [Workshop site](https://project-delphi.github.io/tensors-workshop) ·
[Slides EN](https://project-delphi.github.io/tensors-workshop/slides/en/) ·
[Diapositivas ES](https://project-delphi.github.io/tensors-workshop/slides/es/)

From "I know matrices" to manipulating, solving and factorizing matrices and tensors, in Colab
notebooks with knowledge checks and live deep dives between them. It assumes one chapter of
linear algebra and no tensor theory whatsoever; every term is defined where it first appears. Taught in English, with the slides, handbook and references also in Spanish. Development
and the live site are at
[project-delphi/tensors-workshop](https://github.com/project-delphi/tensors-workshop); the copy here
is a read-only mirror.

## How we work

- **No required paid model APIs.** Workshop labs provide paths without paid model API keys.
  Stockroom runs offline; the NLP labs use open-model downloads or locally trained models.
  Commercial model calls are opt-in, with their usage and cost limits stated.
- **Reproducible numbers.** Figures quoted in a lecture come out of the repository that ships with
  it, in a mode anyone can rerun. Post-mortems are labelled composite or linked to a source. We do
  not invent incidents, companies or statistics to make a point land.
- **Agent = Model + Harness.** Every claim about a failure mode arrives with the test or notebook
  cell that demonstrates it.
- **Yours to teach from.** Fork it, teach it, send a pull request. Each repository carries its own
  contribution guide and licence.

[genial-labs.com](https://genial-labs.com) · [ravi@genial-labs.com](mailto:ravi@genial-labs.com)
