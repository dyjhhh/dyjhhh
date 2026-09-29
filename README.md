# Hi, I'm Yujia 👋

I'm an engineering manager who likes building useful AI products and the systems behind them. My background includes Amazon and Coursera, where I've worked on customer-facing products and data platforms and helped engineers grow.

Outside work, I build a personal agent system with Claude Code and Codex. Running it has given me plenty of practical questions to work through: how an agent picks up where it left off, how to check its output, when to alert a person, and how to turn feedback into a change worth keeping.

These repositories share selected parts of that work. The runnable examples use synthetic data, run offline (`make test` in each repository), and explain what they check and what they leave out.

| Project | What you'll find |
|---|---|
| 🧠 [**Agent OS**](https://github.com/dyjhhh/agent-os) | Architecture notes, sample skills, and a runnable demo of durable task state across sessions. Start here for the overall system. |
| 🧪 [**Agent Eval Gates**](https://github.com/dyjhhh/agent-eval-gates) | Deterministic output checks and a demo that binds artifact review and approval to specific evidence versions. |
| 🛡️ [**Agent Security Hooks**](https://github.com/dyjhhh/agent-security-hooks) | Bounded tool guards, PDF screening, regression tests, and documented limitations. |
| 🚨 [**Agent Reliability**](https://github.com/dyjhhh/agent-reliability) | Offline alert decisions (spaced confirmation, deduplication, caller-reported delivery acknowledgement), successful-work evidence checks, calendar-job replay, and a pre-send output guard. |
| 🔁 [**Self-Improving Loops**](https://github.com/dyjhhh/self-improving-loops) | A small feedback-to-configuration workflow with explicit approval, regression checks, and a traceable receipt. |

These are personal projects built with AI-assisted development: I make the design choices and review the changes, and Claude Code and Codex assist with implementation. I care about being able to explain the design, reproduce the behavior, and recognize where human judgment is still needed.

[LinkedIn](https://www.linkedin.com/in/yujiadong) · [Start with Agent OS](https://github.com/dyjhhh/agent-os)
