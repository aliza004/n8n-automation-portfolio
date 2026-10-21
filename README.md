# n8n Automation Portfolio

Hi, I'm **Aliza Kamran**, an automation engineer in Karachi. I build n8n workflows, AI voice agents, WhatsApp/SMS bots, and automations for web portals that have no API.

This repo holds sanitized, importable examples of that work. All credentials, tokens, hostnames, IDs, and client or company names are replaced with placeholders.

- LinkedIn: https://www.linkedin.com/in/alizakamran04
- Email: aliza.kamran04@gmail.com
- CV: [docs/Aliza_Kamran_CV.pdf](docs/Aliza_Kamran_CV.pdf)

## Workflows

| Workflow | What it shows |
|---|---|
| [portal-account-provisioning-no-api](workflows/portal-account-provisioning-no-api.json) | Automating a web portal with **no API**: loads the login page, extracts the CSRF token and session cookie, logs in, creates an account and subscription through the portal's own requests, and logs every result to Google Sheets. An AI step picks unused usernames, and failures go to an error branch. |
| [whatsapp-intent-bot-with-followups](workflows/whatsapp-intent-bot-with-followups.json) | An LLM classifies each WhatsApp message into 19 intents, a Switch node sends the matching reply, customer state is tracked in a sheet, and a delayed follow-up goes out if the customer goes quiet. |
| [voice-agent-request-email-collection](workflows/voice-agent-request-email-collection.json) | Voice-agent tool endpoint: validates the call, records an expiring request in Postgres, texts the caller via Twilio, returns a spoken-friendly result. |
| [voice-agent-contact-validation-tool](workflows/voice-agent-contact-validation-tool.json) | Voice-agent tool endpoint: normalizes the tool call, looks the caller up in the database, and uses an AI agent with a sub-workflow tool to decide how the call continues. |
| [voice-agent-support-bot-rag](workflows/voice-agent-support-bot-rag.json) | Small voice-agent backend: webhook, Gemini agent, Pinecone knowledge-base tool, response. |
| [sms-send-with-idempotency-and-approval](workflows/sms-send-with-idempotency-and-approval.json) | Production-style SMS API: header auth, validation, idempotency keys for safe retries, contact-policy checks, approval drafts, Twilio delivery, logging, consistent error responses. |

## Patterns used

Webhooks, session/CSRF cookie replay, idempotency keys, retries, error branches, PostgreSQL state, LLM classification, RAG, Twilio, WhatsApp, Vapi voice agents.

## How to import

1. In n8n, open **Workflows > Import from file** and pick a JSON from `workflows/`.
2. Select your own credential in every node that shows a credential warning.
3. Replace the placeholders listed in [docs/PLACEHOLDERS.md](docs/PLACEHOLDERS.md).
4. Run with test data first.

## Responsible use

Only automate portals and accounts you are authorized to use.

## License

MIT, see [LICENSE](LICENSE).
