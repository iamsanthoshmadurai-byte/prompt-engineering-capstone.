# Prompt Engineering Capstone — Prompt Portfolio

## Case Study: Apex Cloud Services CRM Migration

**Business context:** Apex Cloud Services has 150 active sales representatives. Client information is stored in offline spreadsheets, creating fragmented data and making reporting difficult.

**Supplied pricing assumptions from the assignment PDF:**

* Salesforce: $150 per user/month + $25,000 setup
* HubSpot: $90 per user/month + $10,000 setup
* Zoho CRM: $40 per user/month + $5,000 setup

> These are assignment-provided assumptions, not independently verified current vendor quotations. Actual product tiers, contract terms, implementation services, taxes, and add-ons may change total costs.

## Prompt 1 — Meta-Prompting: Generate a CRM Research Prompt

```text
Act as an expert Prompt Engineer. Write a system prompt that turns ChatGPT into a specialized B2B CRM Pricing and Feature Researcher.

The generated system prompt must:
- Focus on Salesforce Enterprise, HubSpot Sales Hub, and Zoho CRM.
- Compare pricing, licensing models, core sales features, customization, integrations, reporting, scalability, implementation effort, and support.
- Distinguish verified facts from estimates and assumptions.
- Request official vendor sources and the date checked for any current pricing claims.
- Never invent licensing terms or features. If a detail cannot be verified, state “Not verified.”
- Use a structured Markdown list and a short comparison table.
- Write the system prompt inside one Markdown code block and nothing else.
```

## Prompt 2 — CO-STAR + Q-GoT Vendor Evaluation

```text
# CONTEXT
Apex Cloud Services is evaluating a CRM for 150 sales representatives. The current process uses offline spreadsheets and suffers from fragmented client data.
Assignment pricing assumptions:
Salesforce: $150/user/month + $25,000 setup.
HubSpot: $90/user/month + $10,000 setup.
Zoho CRM: $40/user/month + $5,000 setup.

# OBJECTIVE
Calculate 1-year and 3-year Total Cost of Ownership (TCO) and compare the options.

# SYSTEM CONTROLS / LOGIC
1. Calculate annual recurring cost = users × monthly price × 12.
2. Calculate 1-year TCO = annual recurring cost + one-time setup.
3. Calculate 3-year TCO = users × monthly price × 36 + one-time setup.
4. Show each arithmetic step and check the totals.
5. Do not add unprovided costs. List possible excluded costs separately.
6. Treat the supplied prices as assignment assumptions, not verified live quotations.

# STYLE
Objective, analytical, finance-first.

# AUDIENCE
CEO and Board of Directors.

# RESPONSE
Show calculations in a Markdown table, identify the lowest-cost option, explain the trade-offs, and state what must be verified before purchasing.
```

## Prompt 3 — Weighted Decision Matrix

```text
Act as a financial analyst. Compare Salesforce, HubSpot, and Zoho for Apex Cloud Services.
Criteria and weights:
- TCO Cost Model: 30%
- Customization \& Scale: 20%
- Setup Speed: 25%
- User Adoption Ease: 25%

Give each vendor a raw score from 1 (poor) to 10 (excellent). Calculate weighted score = raw score × weight as a decimal. Show each multiplication and sum the weighted scores. Ensure weights total 100%.
Explain that non-cost scores are preliminary judgment-based assumptions that should be validated in a pilot; do not present them as measured facts.
```

## Prompt 4 — Six-Month Implementation Roadmap

```text
Act as a project manager. The board has selected HubSpot CRM for the planning scenario.
Create a six-month roadmap:
- Phase 1: Planning \& Data Cleanup (Month 1)
- Phase 2: System Configuration \& Pilot (Months 2–3)
- Phase 3: Full Migration \& Staff Training (Months 4–5)
- Phase 4: Post-Launch Optimization (Month 6)
Show a Markdown or ASCII Gantt chart, key deliverables, owners, and stage-gate checks.
```

## Prompt 5 — Risk Registry

```text
For the HubSpot CRM migration at Apex Cloud Services, identify three implementation risks.
Use a table with Risk Event, Probability (Low/Med/High), Impact (Low/Med/High), and Mitigation. Include data quality/migration, user adoption, and integration/security risks.
```

## Prompt 6 — Executive Presentation

```text
Act as a strategy consultant. Prepare a six-slide executive presentation in Markdown.
Separate slides with exactly three dashes (---).
Slides:
1. Title \& Executive Overview
2. Client Problem \& Current Metrics
3. Vendor Candidates
4. Cost-Benefit Analysis \& TCO
5. Decision Matrix \& Recommendation
6. Phased Roadmap \& Immediate Next Steps
Keep the slides concise and distinguish supplied facts from assumptions.
```

## Prompt 7 — Business Proposal

```text
Write a professional B2B proposal for Apex Cloud Services recommending a CRM migration.
Include executive summary, current-state problem, objectives, vendor comparison, TCO, weighted decision matrix, implementation scope, six-month roadmap, risks and mitigations, success measures, exclusions, and next steps. Use the supplied assignment pricing assumptions and label score-based judgments as preliminary.
```

## Prompt 8 — Lessons Learned

```text
Write a lessons-learned post-mortem for an AI-assisted CRM selection project.
Cover hallucination prevention, arithmetic verification, long-context limitations and prompt chaining, and when to use RGCCO, CARE, ERA, or CO-STAR. Explain limitations and human review needs.
```

## Prompt 9 — Quality Review

```text
Act as an independent QA reviewer. Check the project deliverables for:
- Arithmetic correctness
- Weights totaling 100%
- Consistency between the cost analysis, matrix, recommendation, and roadmap
- Clearly labeled assumptions and unverified claims
- Exactly six presentation slides
- Three risks with actionable mitigations
- No fabricated URLs, quotations, or results
Return a checklist of issues and suggested fixes.
```

