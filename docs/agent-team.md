# Agent team

Mona's Project Pulse dashboard will be built with a coordinated team of specialist GitHub Copilot CLI agents in a Codespace. The workflow is centered on orchestration: the Orchestrator delegates work to specialist agents instead of doing the implementation in one undifferentiated prompt.

## Orchestrator
- Model: Claude Opus 4.7 (copilot)
- Responsibility: coordinates the overall task, breaks work into phases, delegates to the Planner, Designer, and Coder, and verifies that the integrated result matches the brief.
- Definition: `.github/agents/orchestrator.agent.md`

## Planner
- Model: Claude Opus 4.7 (copilot)
- Responsibility: researches the repo and project brief, identifies phases, dependencies, and validation expectations, and creates a practical implementation plan before coding starts.
- Definition: `.github/agents/planner.agent.md`

## Designer
- Model: Gemini 3.1 Pro (copilot)
- Responsibility: shapes the user experience and visual design for the dashboard, including hierarchy, usability, responsiveness, accessible UI, and polished styling cues such as cards, badges, spacing, and shadows.
- Definition: `.github/agents/designer.agent.md`

## Coder
- Model: GPT-5.5 (copilot)
- Responsibility: implements the static dashboard files and any required support configuration, such as the VS Code launch file that previews the app from the `app/` directory.
- Definition: `.github/agents/coder.agent.md`

Together, this team will use GitHub Copilot CLI in the Codespace terminal to inspect the repo, plan the dashboard work, divide design from implementation, validate the result, and hand off a runnable Project Pulse experience.
