# n8n Automation Portfolio

Five independent n8n workflow projects for repetitive business tasks, with
structured LLM outputs and explicit human review paths. The repositories include
importable workflows, setup instructions, and screenshots; documented checks cover
n8n 2.33.3 imports, connections, schemas, and Code-node logic.

**Start here:** [SupportPilot AI](https://github.com/pihuts/supportpilot-ai) for
ticket classification and escalation, or
[OutreachEngine AI](https://github.com/pihuts/outreachengine-ai) for source-grounded
drafting with human review. For executable tests and a recorded receipt vision-chain
demo, see my separate [receipt/email assessment](https://github.com/pihuts/pds-n8n-portfolio).

These are portfolio implementations. Full execution requires configured service
credentials; the checks above do not represent five live client deployments.

| Project | Category | What it does |
|---|---|---|
| [CareerCompass AI](https://github.com/pihuts/careercompass-ai) | Career | Scrapes HN hiring threads, scores jobs against your profile, drafts cover letters |
| [SupportPilot AI](https://github.com/pihuts/supportpilot-ai) | Customer support | Classifies tickets, drafts replies, escalates low-confidence cases |
| [OutreachEngine AI](https://github.com/pihuts/outreachengine-ai) | Sales | Writes personalized outreach grounded in each lead's real website |
| [LedgerLens AI](https://github.com/pihuts/ledgerlens-ai) | Finance ops | Extracts structured invoice data from PDFs |
| [ActionFlow AI](https://github.com/pihuts/actionflow-ai) | Productivity | Turns transcripts into summaries, decisions, and tracked action items |

## Why these projects

Each workflow demonstrates a concrete automation use case:

- AI customer support and ticket automation
- AI sales development and personalized outreach
- Document AI and finance operations
- Meeting intelligence and productivity automation
- Agentic workflows with LLM structured output

## Shared stack

- n8n (webhooks, forms, schedules, branches)
- OpenAI GPT-5.6 family (Sol / Terra / Luna) with strict JSON schemas
- Google Sheets as a lightweight data layer
- Gmail for human-in-the-loop notifications
- Environment variables for configuration

Model mapping:

| Project | Model |
|---|---|
| CareerCompass AI | `gpt-5.6-sol` (flagship reasoning) |
| SupportPilot AI | `gpt-5.6-luna` (fast, high-volume) |
| OutreachEngine AI | `gpt-5.6-terra` (balanced writing) |
| LedgerLens AI | `gpt-5.6-luna` (fast extraction) |
| ActionFlow AI | `gpt-5.6-terra` (balanced analysis) |

## Test status

Each workflow:

- Imports successfully into n8n 2.33.3 (`n8n import:workflow`)
- Has valid node connections and unique node names
- Passes code-node logic tests with sample data

This repo is the index. Each project has its own public repository with the importable n8n workflow JSON, README, and workflow screenshot.

End-to-end execution requires your own OpenAI, Google Sheets, and Gmail credentials. The AI and persistence nodes are intentionally left unconfigured so you connect your accounts.
