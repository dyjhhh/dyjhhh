# Hi, I'm Yujia 👋

I'm an engineering manager who likes building useful AI products and the systems behind them. My background includes Amazon and Coursera, where I've worked on customer-facing products and data platforms and helped engineers grow.

Outside work, I build a personal agent system with Claude Code and Codex. Running it has given me plenty of practical questions to work through: how an agent picks up where it left off, how to check its output, when to alert a person, and how to turn feedback into a change worth keeping.

These repositories share selected parts of that work. The runnable examples use synthetic data, run offline (`make test` in each repository), and explain what they check and what they leave out.

| Project | What you'll find |
|---|---|
| 🧠 [**Agent OS**](https://github.com/dyjhhh/agent-os) | Architecture notes, sample skills, and a runnable demo of durable task state across sessions. Start here for the overall system. |
| 🧪 [**Agent Eval Gates**](https://github.com/dyjhhh/agent-eval-gates) | Deterministic output checks and a demo that binds artifact review and approval to specific evidence versions. |
| 🛡️ [**Agent Security Hooks**](https://github.com/dyjhhh/agent-security-hooks) | Bounded tool guards, PDF screening, regression tests, and documented limitations. |
| 🚨 [**Agent Reliability**](https://github.com/dyjhhh/agent-reliability) | Real incidents turned into small modules with failure-path tests: alert deduplication and delivery acknowledgement, inbox-to-ledger reconciliation, listeners that are alive but no longer receiving, tests kept out of real state, and usage-limit refusals that do not use up a daily cap. |
| 🔁 [**Self-Improving Loops**](https://github.com/dyjhhh/self-improving-loops) | A small feedback-to-configuration workflow with explicit approval, regression checks, and a traceable receipt. |
| 🔔 [**Award Alert Bridge**](https://github.com/dyjhhh/award-alert-bridge) | Time-critical alerts for inventory that can vanish in minutes: one event key across email and API sources, multichannel wake with a finite repeat ceiling, acknowledgement from a single inbound queue, gated re-arming of one-shot alerts, and health notices sent once per fault. No booking or payment code. |
| 📋 [**Careers Watch**](https://github.com/dyjhhh/careers-watch) | A change feed over several hundred public job-board APIs (Greenhouse, Ashby, Lever, Workday): exact posting identity, a zero-token prefilter that decides which few postings reach a model, bounded scoring batches, and usage-limit refusals that keep the queue and charge nothing. |

These are personal projects built with AI-assisted development: I make the design choices and review the changes, and Claude Code and Codex assist with implementation. I care about being able to explain the design, reproduce the behavior, and recognize where human judgment is still needed.

[LinkedIn](https://www.linkedin.com/in/yujiadong) · [Start with Agent OS](https://github.com/dyjhhh/agent-os)
