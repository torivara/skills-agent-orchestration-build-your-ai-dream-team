# Agent team

For Mona's Project Pulse dashboard, I will use a custom four-agent team orchestrated through GitHub Copilot CLI in a Codespace.

- **Orchestrator** — Model: Claude Opus 5.5 (copilot). Breaks the work into phases, delegates tasks with explicit file scopes, coordinates dependencies and parallel work, and verifies the integrated result. Definition: `.github/agents/orchestrator.agent.md`
- **Planner** — Model: Claude Opus 5.5 (copilot). Researches the repository and relevant technical details, then produces an actionable plan covering ordered steps, file ownership, dependencies, risks, edge cases, and validation. Definition: `.github/agents/planner.agent.md`
- **Coder** — Model: GPT-5.5 (copilot). Implements assigned code changes, fixes bugs, adds assigned runnable-app support, and validates behavior while staying within the agreed file scope. Definition: `.github/agents/coder.agent.md`
- **Designer** — Model: Gemini 3.7 Flash (copilot). Shapes the dashboard's user experience, including usability, accessibility, information hierarchy, interaction flow, responsive behavior, and visual design. Definition: `.github/agents/designer.agent.md`

The Planner researches the project and gives the Orchestrator a practical implementation plan. The Orchestrator assigns scoped tasks to the Designer and Coder, allowing their work to proceed in parallel when file ownership and dependencies permit, and sequencing work when it does not. The Orchestrator then checks that the design and implementation fit together, verifies the finished dashboard, and reports the outcome.
