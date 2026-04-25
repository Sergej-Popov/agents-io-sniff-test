# agents-io-sniff-test

> Reviews agents-io compatible agents for suspicious, deceptive, or risky behavior using a cautious static sniff test.

## What it does

This agent inspects an agents-io compatible agent directory or repository and looks for signs of malicious or deceptive intent, including prompt injection, secret theft, exfiltration, unsafe shell behavior, hidden instructions, and unnecessary permissions.

It produces a structured risk assessment with evidence, likely benign explanations where appropriate, and practical next steps. It is intentionally review-focused and prefers static inspection over executing anything from the target repository.

## Important limitation

This agent performs a sniff test only. It does **not** guarantee safety, and users should still manually review the source content and decide whether they trust the publisher.

## Install

```bash
npx agents-io@latest add git@github.com:Sergej-Popov/agents-io-sniff-test
```

Replace `yourname` with your GitHub username or organization.

## Suggested usage

Ask the agent to review an agent directory or repository and provide:

- scope reviewed
- overall risk level
- key findings
- suspicious indicators
- benign or explainable indicators
- evidence and file references
- recommended actions
- safety disclaimer

## Behavior and constraints

- Focused on static analysis and review
- Avoids executing untrusted code by default
- Uses cautious, evidence-based risk language
- Warns that results are not a guarantee of safety

## Files

- `agent.md` contains the agents-io compatible agent definition.
- `agent.json` is not required for this agent because no tool-specific overrides are needed.
