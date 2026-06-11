# Paul the Octopus

[English](README.md) | [中文](README.zh-CN.md)

Paul the Octopus is a football score prediction companion with a playful matchday personality. It looks at the pre-match picture, weighs the key football variables, invites a small expert-style panel into the tank, and then taps one scoreline with its tentacle.

Use it before World Cup matches, continental tournaments, national-team fixtures, or important club games when you want more than a bare prediction. Paul keeps the forecast traceable, shows where the uncertainty is, and still leaves room for a little octopus theatre.

> For entertainment only. This is not betting advice.

## What It Does

- Predicts the score for a clearly identified football match.
- Summarizes the pre-match situation in six compact lines: fixture, squad, injuries, dressing room, form/head-to-head, and environment.
- Uses a short source index instead of long article summaries.
- Proposes 3-5 football experts or analysts as a simulated `Paul-chartroom` panel before the final call.
- Separates facts, rumors, simulated expert views, and Paul's final judgment.
- Returns the most likely score, 1-2 alternative scores, match-result lean, confidence level, and key swing variable.

## What It Does Not Do

- It does not scrape, summarize, or rely on betting-market pages.
- It does not provide staking plans, arbitrage ideas, bankroll allocation, or guaranteed outcomes.
- It does not treat unsourced social rumors as facts.
- It does not predict when the match identity is unclear.

## Installation

Place this repository in your local skills directory:

```bash
cd ~/.codex/skills
git clone https://github.com/Hchen1218/Paul-the-Octopus.git paul-the-octopus
```

Then invoke it with `$paul-the-octopus`, or ask for a football score prediction directly.

## Example Prompts

```text
Use Paul the Octopus to predict the 2026 World Cup opener: Mexico vs South Africa. First give me the pre-match intelligence and Paul-chartroom panel nominees, then wait for my confirmation.
```

```text
Paul the Octopus, predict the United States' first 2026 World Cup match. Show me the expert panel first.
```

```text
For the same match, reuse the fixture and squad facts we already checked. Only refresh injuries, press-conference updates, and venue conditions.
```

## Workflow

1. Lock the match: teams, competition, date, venue, phase, and kickoff context.
2. Verify public information with a compact search pass.
3. Build the six-line pre-match intelligence brief.
4. Nominate a 3-5 person `Paul-chartroom` panel based on the blind spots in this match.
5. Wait for the user to confirm or adjust the panel.
6. Give the expert results first, then Paul's score prediction and entertainment disclaimer.

## Repository Layout

```text
.
├── README.md
├── README.zh-CN.md
├── SKILL.md
├── LICENSE
├── .gitignore
├── agents/
│   └── openai.yaml
├── evals/
│   └── evals.json
└── references/
    ├── paul-chartroom.md
    ├── report-template.md
    └── source-policy.md
```

- `SKILL.md`: entry point, trigger rules, and main workflow.
- `references/source-policy.md`: source priority, search budget, and prohibited source types.
- `references/paul-chartroom.md`: panel selection, meeting format, and Paul's final judgment rules.
- `references/report-template.md`: two-stage chat output template.
- `evals/evals.json`: baseline behavior checks.

## Quality Bar

Every prediction should:

- Use current public sources and include real links.
- Keep the source index short and relevant.
- Clearly distinguish verified facts, weak rumors, simulated expert analysis, and Paul's final call.
- Stop the first response at panel nomination unless the user has already asked to proceed directly.
- Put expert results before Paul's final score prediction.
- Include the entertainment disclaimer and avoid betting advice.

## License

MIT
