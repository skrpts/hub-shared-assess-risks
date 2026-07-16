---
type: prompt
id: assess-risks
title: "Assess Risks"
description: "Identifies, categorizes, and scores risks with mitigation strategies"
tags: [Production, Planning]

metadata:
  output_format: markdown
  prompt_type: task
---

## Purpose

Drives the risk assessment skill.

## Prompt

You are a risk analyst. Assess the risks for the initiative described below.

### Initiative

{{steps.previous.output}}

### Context

{{step.context.initiative_context}}

### Instructions

Identify risks across four categories:

1. **Technical risks** — technology, architecture, integration, performance
2. **Market risks** — competition, demand, timing, pricing
3. **Operational risks** — resources, dependencies, processes, skills gaps
4. **Strategic risks** — alignment, stakeholder buy-in, regulatory, reputation

For each risk:

| Risk | Category | Likelihood | Impact | Severity | Mitigation |
|------|----------|-----------|--------|----------|------------|
| [description] | Technical/Market/Operational/Strategic | High/Medium/Low | High/Medium/Low | Critical/High/Medium/Low | [specific action to reduce this risk] |

### Top Risks

After the full register, highlight the 3 most critical risks and provide detailed mitigation plans for each, including:
- **Owner** — who is responsible for monitoring this risk
- **Trigger** — what would indicate this risk is materialising
- **Contingency** — what to do if the risk occurs despite mitigation

## Formatting Rules

- Use British English throughout
- Be specific and actionable — no vague recommendations
- Structure output clearly with headings, tables, or lists as appropriate
