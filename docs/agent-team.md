# Agent team

For Mona's Project Pulse dashboard, I will use a custom four-agent team defined under the repository's agent folder and orchestrated through GitHub Copilot CLI in a GitHub Codespace.

- Planner — Model: auto (copilot). Responsible for researching the codebase, checking dependencies and edge cases, and producing an implementation plan with ordered steps, file assignments, sequencing, and validation expectations. Definition: `.github/agents/planner.agent.md`
- Orchestrator — Model: auto (copilot). Responsible for breaking the work into phases, delegating tasks to the specialist agents, tracking dependencies, and verifying that the final result fits together. Definition: `.github/agents/orchestrator.agent.md`
- Designer — Model: auto (copilot). Responsible for the product experience: UI/UX, accessibility, information hierarchy, interaction flow, and the visual design of the dashboard. Definition: `.github/agents/designer.agent.md`
- Coder — Model: auto (copilot). Responsible for implementing the actual code, fixing bugs, handling file-scoped changes, adding runnable app support when needed, and validating behavior before reporting completion. Definition: `.github/agents/coder.agent.md`

This setup keeps planning, design, implementation, and coordination clearly separated while using GitHub Copilot CLI in a Codespace to manage the overall workflow for the Project Pulse build.
