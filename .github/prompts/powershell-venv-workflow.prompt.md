---
name: PowerShell Venv Workflow
description: "Generate safe PowerShell command workflows for this Windows workspace with .venv active."
argument-hint: What do you want to do in this shell session?
agent: agent
---
Use this prompt to help with repeatable terminal work in this workspace.

Execution context:
- Shell: Windows PowerShell
- Prompt: (.venv) PS A:\VHU>
- Working directory: A:\VHU
- Python virtual environment: .venv is active

Use the text provided when this prompt is invoked as the user goal.

If the invocation text is missing or appears to be only shell context (for example, just a prompt string), ask one concise clarifying question before proposing commands.

When a valid goal is provided, respond with:
1. A short plan (3 to 5 steps).
2. Exact PowerShell commands in execution order.
3. Quick verification checks to confirm success.
4. A short safety note if any command is destructive or irreversible.

Rules:
- Use PowerShell-native syntax, not bash syntax.
- Prefer safe, reversible actions first.
- Keep commands copy-paste ready.
- Assume paths are relative to A:\VHU unless absolute paths are required.
- For Python tasks, use the active .venv environment.