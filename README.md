# Hi, I'm Yujia 👋

I'm an engineering manager and a player-coach: I build AI agent harnesses, meaning the workflows, orchestration and tools around Claude Code and Codex, and I run them in daily use. A team gets patterns that have already broken in practice and been fixed, with the incident write-ups below.

My background includes Amazon and Coursera, where I've worked on customer-facing products and data platforms and helped engineers grow.

## Lessons

Five incidents from running always-on agents, each written up in public, and the rule each one left behind:

1. [**Done means the outcome was confirmed, not that a step ran**](https://github.com/dyjhhh/agent-reliability/blob/main/docs/operations-notes.md#marked-seen-is-not-delivered): a pipeline marked a message seen before delivering it, and every health check stayed green while the message was never forwarded.
2. [**A live process is not a working agent**](https://github.com/dyjhhh/agent-reliability/blob/main/docs/operations-notes.md#alive-is-not-receiving): after five silent days, a watchdog that only checked the process could not tell a quiet chat from a listener that had stopped receiving.
3. [**Every fact needs exactly one owner**](https://github.com/dyjhhh/agent-os/blob/main/docs/incidents.md): a closed item kept returning in scheduled reports because copies lived in several files and the report read a stale one (incident 1).
4. [**Keep tests out of production state by construction, not by convention**](https://github.com/dyjhhh/agent-reliability/blob/main/docs/operations-notes.md#tests-must-not-see-the-real-home): one test run used the real home directory, wrote into production history and triggered recovery notices for outages that never happened.
5. [**Missing proof is not a failure**](https://github.com/dyjhhh/agent-reliability/blob/main/docs/operations-notes.md#expired-evidence-is-not-an-outage): expired end-to-end test evidence paged as an outage for about 32 hours, so aged evidence now becomes one retest reminder while real failures still page.

The common thread is [principle 2](https://github.com/dyjhhh/agent-os/blob/main/docs/principles.md#2-a-proxy-signal-never-carries-the-heaviest-conclusion): a cheap proxy signal should never carry the most expensive conclusion.

## Projects

These repositories share selected parts of that work. The runnable examples use synthetic data, run offline (`make test` in each repository), and explain what they check and what they leave out.

| Project | What you'll find |
|---|---|
| 🧠 [**Agent OS**](https://github.com/dyjhhh/agent-os) | Architecture notes, sample skills, and a runnable demo of durable task state across sessions. Start here for the overall system. |
| 🧪 [**Agent Eval Gates**](https://github.com/dyjhhh/agent-eval-gates) | Deterministic output checks and a demo that binds artifact review and approval to specific evidence versions. |
| 🛡️ [**Agent Security Hooks**](https://github.com/dyjhhh/agent-security-hooks) | Bounded tool guards, PDF screening, regression tests, and documented limitations. |
| 🚨 [**Agent Reliability**](https://github.com/dyjhhh/agent-reliability) | Real incidents turned into small modules with failure-path tests: alert deduplication and delivery acknowledgement, inbox-to-ledger reconciliation, listeners that are alive but no longer receiving, tests kept out of real state, and usage-limit refusals that do not use up a daily cap. |
| 🔁 [**Self-Improving Loops**](https://github.com/dyjhhh/self-improving-loops) | A small feedback-to-configuration workflow with explicit approval, regression checks, and a traceable receipt. |
| 🔔 [**Award Seat Alerter**](https://github.com/dyjhhh/award-seat-alerter) | Time-critical alerts for inventory that can vanish in minutes: one event key across email and API sources, multichannel wake with a finite repeat ceiling, acknowledgement from a single inbound queue, gated re-arming of one-shot alerts, and health notices sent once per fault. No booking or payment code. |
| 📋 [**Career Watcher**](https://github.com/dyjhhh/career-watcher) | A change feed over several hundred public job-board APIs (Greenhouse, Ashby, Lever, Workday): exact posting identity, a zero-token prefilter that decides which few postings reach a model, bounded scoring batches, and usage-limit refusals that keep the queue and charge nothing. |

These are personal projects built with AI-assisted development: I make the design choices and review the changes, and Claude Code and Codex assist with implementation. I care about being able to explain the design, reproduce the behavior, and recognize where human judgment is still needed.

[LinkedIn](https://www.linkedin.com/in/yujiadong) · [Start with Agent OS](https://github.com/dyjhhh/agent-os)
