# Sample system prompts for the OpenClaw Agent template

Drop-in directives for the `systemPrompt` form field when creating
common role-presets through the OpenClaw Agent template. Copy the
markdown into the Directive textarea; pair it with the matching
role + capabilities below.

| File | Use for | Role + capabilities to pair with |
|---|---|---|
| `pm-agent-system-prompt.md` | Project Manager agent — interviews stakeholders, plans projects as GitHub Issues + Projects v2 cards, hands off to specialist agents. | `role: pm`, `capabilities: [project-intake, task-decomposition, agent-inventory, cross-agent-context-bridging]`. Also enable: **Federate GitHub MCP**, attach KB: **agent-platform-capabilities**, set Discord URL to the stakeholder channel. |

Add more presets to this directory as new role conventions stabilize.
Pattern is: a short `<role>-system-prompt.md` file + one row in the
table above naming the role + capabilities + recommended form
toggles.
