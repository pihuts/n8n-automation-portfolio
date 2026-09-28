# n8n Automation Portfolio

Five independent workflows for support triage, invoice intake, grounded outreach drafts, meeting actions and job scouting. Built with n8n, structured LLM outputs, webhooks/HTTP APIs, Google Sheets and Gmail.

**Updated September 2026:** dry-run and enable controls, validated inputs, stable-key duplicate checks, bounded execution, failure alerts and operator recovery instructions. **25 offline smoke tests pass** across the five repositories; GitHub Actions runs each repository's checks.

| Project | Problem and implementation | Inspect |
|---|---|---|
| [SupportPilot AI](https://github.com/pihuts/supportpilot-ai) | Authenticated ticket intake, structured reply suggestions and human escalation with delivery tracking | [Tests](https://github.com/pihuts/supportpilot-ai/blob/main/smoke_test.py) |
| [LedgerLens AI](https://github.com/pihuts/ledgerlens-ai) | PDF invoice extraction, vendor/invoice duplicate keys and finance review; no payment or approval | [Tests](https://github.com/pihuts/ledgerlens-ai/blob/main/smoke_test.py) |
| [OutreachEngine AI](https://github.com/pihuts/outreachengine-ai) | Validated leads and website evidence to Gmail drafts; thin sources need human review | [Tests](https://github.com/pihuts/outreachengine-ai/blob/main/smoke_test.py) |
| [ActionFlow AI](https://github.com/pihuts/actionflow-ai) | Authenticated meeting transcripts to summaries, decisions, action items and notification tracking | [Tests](https://github.com/pihuts/actionflow-ai/blob/main/smoke_test.py) |
| [CareerCompass AI](https://github.com/pihuts/careercompass-ai) | HN hiring posts to profile-based scores, cover-letter drafts and a Manila-time digest | [Tests](https://github.com/pihuts/careercompass-ai/blob/main/smoke_test.py) |

## What the checks establish

Each project includes importable workflow JSON, a failure-alert workflow, setup instructions, screenshots, fixtures and `python smoke_test.py`. Five checks per repository cover graph/JavaScript validity, preflight modes, input edges, replay/network cases and write guards. The 25-check result was reproduced locally on 29 September 2026.

Dry run is the default. Full execution requires your own n8n instance, configured credentials and environment settings. Follow each README's test-account and go-live checklist before using real data. Offline tests do not establish live Google/OpenAI connectivity, measured LLM accuracy or client deployment.

Google Sheets lookup/upsert prevents ordinary sequential duplicates but has no atomic uniqueness constraint. The runbooks explain concurrency limits and recovery after uncertain writes or email delivery. Human review remains explicit: support replies are suggestions, finance approves invoices, and outreach stays in drafts.

## More evidence

My separate [receipt and email automation assessment](https://github.com/pihuts/pds-n8n-portfolio) includes executable JavaScript tests and a recorded receipt vision-chain demo.

[Portfolio](https://pihuts.netlify.app/) ? [GitHub profile](https://github.com/pihuts) ? [LinkedIn](https://www.linkedin.com/in/peter-gino-pangapalan-78219433a/)
