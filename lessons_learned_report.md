# Lessons Learned Post-Mortem Report

## AI-Assisted CRM Selection — Apex Cloud Services

## 1\. Project summary

This capstone used prompt engineering to support a CRM vendor comparison and implementation plan for Apex Cloud Services, which has 150 sales representatives and currently stores client information in offline spreadsheets. AI helped structure the work into prompts, cost calculations, a decision matrix, a roadmap, risks, and presentation materials.

AI output is a draft for review, not automatic proof that a vendor is suitable or that a claim is correct.

## 2\. Hallucination prevention and verification

Large language models can produce plausible but incorrect facts, including pricing, feature descriptions, or licensing details. The project reduced this risk by:

* Treating the prices in the assignment as explicit assumptions.
* Avoiding claims that these prices are current vendor quotations.
* Asking for verified vendor sources and a date checked when researching current product facts.
* Marking unavailable details as “Not verified” instead of guessing.
* Separating assignment facts, calculations, and judgment-based scores.

A final procurement decision should be based on official vendor documentation, written quotations, security review, and a pilot.

## 3\. Step-by-step arithmetic audit

The TCO formulas were written explicitly:

* 1-year TCO = 150 × monthly price × 12 + setup fee.
* 3-year TCO = 150 × monthly price × 36 + setup fee.

Rechecking each multiplication and addition produced:

* Salesforce: $295,000 for one year; $835,000 for three years.
* HubSpot: $172,000 for one year; $496,000 for three years.
* Zoho CRM: $77,000 for one year; $221,000 for three years.

This arithmetic audit helps catch mistakes, but it does not verify whether the input prices accurately represent a real product tier or contract.

## 4\. Context-window limitations and prompt chaining

Long conversations can make it harder to keep every earlier constraint prominent. A model may overlook requirements or mix assumptions across tasks. Useful practices include:

* Start a clean chat for a distinct task when context becomes confusing.
* Keep a concise project brief with fixed facts, assumptions, formulas, and output requirements.
* Break work into stages: research prompt, cost calculations, matrix, roadmap, proposal, presentation, and QA.
* Reuse approved outputs as inputs to the next stage.
* Ask for a final consistency check across all files.

Prompt chaining makes the workflow easier to inspect, but every stage still needs human review.

## 5\. Framework alignment

### RGCCO — creative or copy-oriented tasks

Use Role, Goal, Context, Constraints, and Output format to guide writing such as marketing copy or a structured blog post. It is useful when tone and format matter.

### CARE — interactive dialogues

Use CARE when a task requires a conversational exchange, such as clarifying a user's needs and responding empathetically. Confirm the exact expansion of the framework if a course defines it differently.

### ERA — quick queries

Use ERA for short, direct questions that need a focused answer. Confirm the framework's course-specific definition if required by the assignment.

### CO-STAR — presentations and proposals

Use Context, Objective, Style, Tone, Audience, and Response to make business outputs clearer. It is well suited to an executive proposal or board presentation because it specifies both audience and deliverable.

Framework names can be defined differently in different courses. Use the definitions taught by the instructor if they differ from these practical descriptions.

## 6\. Q-GoT and decision-making

A Quantitative Graph of Thoughts (Q-GoT) style of prompt asks the model to explore related calculations or decision branches and check arithmetic. In this project, explicit formulas and step-by-step totals made the cost comparison easier to audit.

However, a structured reasoning prompt does not guarantee factual accuracy. Scores for setup speed, customization, and adoption were illustrative assumptions, not measured outcomes. The 0.05-point difference between HubSpot and Zoho is too small to justify a decision without further evidence.

## 7\. What went well

* The project was divided into manageable deliverables.
* The TCO method was explicit and reproducible.
* Weights were checked to total 100%.
* The roadmap included stage gates and owners.
* Risks were connected to practical mitigation actions.

## 8\. What should improve

* Verify current licensing and pricing through official vendor sources.
* Define business and technical requirements before assigning feature scores.
* Run a pilot with representative sales users.
* Measure baseline data quality and reporting time before setting targets.
* Add implementation, integration, training, tax, and support costs when reliable quotations are available.
* Obtain security and privacy review before migrating customer data.

## 9\. Conclusion

Prompt engineering can improve the consistency, structure, and auditability of business analysis. It cannot replace source verification, arithmetic checks, stakeholder input, or accountable human decisions. The responsible result is a conditional recommendation with clearly labeled assumptions and a plan for validating them.

