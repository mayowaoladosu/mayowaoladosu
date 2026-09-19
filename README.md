# Oluwamayowa Oladosu

I build backend systems, web applications, and cloud deployment tools. My work focuses on the parts that make services usable: APIs, billing, deployment recovery, networking, and clear operational workflows.

I'm interested in backend, full-stack, and platform engineering opportunities.

[Portfolio](https://oluwamayowa.vercel.app) · [Email](mailto:ceo@layerrail.com) · [X](https://x.com/oluwamayowa)

**Tools I work with:** Python · Ruby · TypeScript · Go · React / Next.js · PostgreSQL · Docker · GitHub Actions

## Selected work

### [LayerRail](https://github.com/Layerrail/layerrail) — cloud control plane

I develop a Ruby/PostgreSQL cloud control plane built on Ubicloud. My contributions include [invoice delivery with retries and duplicate prevention](https://github.com/Layerrail/layerrail/commit/a1a8d43a3e98d07c90f93757c62b42214bcaed2b), usage limits, provider integrations, and Kubernetes networking fixes. The repository retains its upstream attribution.

- **Explore:** [Website](https://layerrail.com) and [architecture](https://github.com/Layerrail/layerrail#architecture).
- **Local walkthrough:** [Docker quick start](https://github.com/Layerrail/layerrail#quick-start) opens the control plane at `localhost:3000`; use Linux, macOS, or WSL.
- **Validation:** [RSpec setup and commands](https://github.com/Layerrail/layerrail/blob/layerrail-rebrand-start/DEVELOPERS.md#running-the-tests). The linked billing change includes tests for retries, transaction rollback, and duplicate delivery.
- **Current scope:** Active development. Real cloud provisioning requires provider credentials and running workers; opening the local console alone does not exercise those operations.

### [Meshferry](https://github.com/mayowaoladosu/meshferry) — tunnels from terminal to dashboard

A TypeScript application connecting a CLI agent, Next.js dashboard, PostgreSQL control plane, and WebSocket gateway. It implements terminal approval, subdomain ownership, and HTTP/TCP/UDP forwarding.

- **Local walkthrough:** Approve a terminal, expose a local HTTP service, then inspect requests and latency in the dashboard. [Setup instructions](https://github.com/mayowaoladosu/meshferry#quick-start) require PostgreSQL/Neon and `DATABASE_URL`.
- **Validation:** After building and configuring the database, `npm run smoke` exercises approval, HTTP forwarding, and persisted telemetry. [Read the test](https://github.com/mayowaoladosu/meshferry/blob/main/scripts/smoke.mjs).
- **Current scope:** Development prototype. The smoke test covers HTTP; TCP/UDP behavior and authorization edge cases need broader automated coverage before a production-readiness claim.

### [devvpush — development branch](https://github.com/mayowaoladosu/devvpush/tree/staging)

My extension of the open-source DevPush platform adds deployment recovery, remote-node management, scoped API tokens, observability, and a Python CLI. These additions are on **`staging`**; `main` contains the upstream baseline.

- **Local walkthrough:** Follow the [Docker Compose quick start](https://github.com/mayowaoladosu/devvpush/blob/staging/README.md#local-quickstart), using `git clone --branch staging --single-branch https://github.com/mayowaoladosu/devvpush.git layerrail`. Configure a GitHub App and the required secrets before starting.
- **Validation:** [Foundation CI passed on July 30, 2026](https://github.com/mayowaoladosu/devvpush/actions/runs/30545167810) at `0f6c2e6`, covering application/CLI tests, container builds, migrations, BuildKit isolation, and node-agent tests. [Local validation commands](https://github.com/mayowaoladosu/devvpush/blob/staging/README.md#validation).
- **Current scope:** Development branch with source and CI evidence. The quick start describes local deployment; hosted and production-scale results are not documented here.

### [DeployTide](https://github.com/mayowaoladosu/DeployTide) — managed deployment platform in development

A deployment platform derived from the Apache-licensed portions of Dokploy. My work includes a [framework detector](https://github.com/mayowaoladosu/DeployTide/commit/0248275bfa0cfe8313c7a4bac5e5bd4fc63521ef), workspace ownership boundaries, capacity scheduling, and a Go runtime controller.

- **Local walkthrough:** [Development setup](https://github.com/mayowaoladosu/DeployTide/blob/deploytide/CONTRIBUTING.md#setup) uses Node.js 24, pnpm, PostgreSQL, Redis, and Docker.
- **Validation:** [Foundation CI passed on August 4, 2026](https://github.com/mayowaoladosu/DeployTide/actions/runs/30896068473) at `0248275`. [Validation notes](https://github.com/mayowaoladosu/DeployTide/blob/deploytide/docs/validation/phase4.md) describe the tested infrastructure components and remaining gaps.
- **Current scope:** Active development, with no public service endpoint advertised. The provisioning templates render infrastructure configuration; real provider lifecycle integration remains future work in the linked validation notes.

### [Offline Agriculture Advisor](https://github.com/mayowaoladosu/adtc-laptop-llm) — CPU-only AI demonstration

A Python/llama.cpp project using quantized Qwen2.5-3B, static offline field guides, and deterministic output checks for two agriculture prompts.

- **Watch:** [104-second recorded demo](https://youtu.be/jPYHFnK15Q4) and [raw generated answers](https://github.com/mayowaoladosu/adtc-laptop-llm/blob/main/docs/evidence/demo-transcript.json).
- **Reproduce:** [Model download and profiler instructions](https://github.com/mayowaoladosu/adtc-laptop-llm#reproduce-locally).
- **Measured results:** [Committed benchmark output](https://github.com/mayowaoladosu/adtc-laptop-llm/blob/main/docs/evidence/submission.json) reports **13.41 tokens/sec**, **3,458.86 MB peak RSS**, and **0.80 ARC-Easy acc_norm across 50 samples** on a GitHub Actions CPU runner.
- **Current scope:** A bounded demonstration. Those results do not establish agricultural accuracy beyond the examples or performance on every laptop; there is no fine-tuning or general retrieval pipeline.

## Open-source contribution

[Cloud Steward incident callback](https://github.com/CALLE-AI/awesome-phone-call-agents/pull/70) — a Python contribution merged into CALL-E's agent examples on September 11, 2026, with tests using a simulated provider and explicit confirmation boundaries for incident notifications.

---

Evidence last checked September 19, 2026. CI results apply to the linked commits. Local setup guides and tests are provided for reproduction; only explicitly linked CI runs and benchmark artifacts are reported here as completed validation.
