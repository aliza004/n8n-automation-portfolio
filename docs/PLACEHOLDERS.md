# Placeholders to replace after import

| Placeholder | Meaning |
|---|---|
| `YOUR_CREDENTIAL_ID` | Select your own credential in each node that shows a credential warning |
| `YOUR_GOOGLE_SHEET_ID` | Your Google Sheet document ID |
| `YOUR_INSTANCE_ID`, `YOUR_INSTANCE_TOKEN`, `YOUR_Z_API_CLIENT_TOKEN` | WhatsApp provider instance values |
| `YOUR_PORTAL_USERNAME`, `YOUR_PORTAL_PASSWORD` | Login for a portal you are authorized to automate |
| `portal.example.com`, `links.example.com` | Your portal and link-service hosts |
| `YOUR-N8N-HOST` | Your n8n host |
| `YOUR_SUBWORKFLOW_ID`, `YOUR_IDEMPOTENCY_WORKFLOW_ID` | IDs of helper workflows the main workflow calls (not included) |
| `[your-link]`, `[price]`, `[account info]`, `[discount-link]`, `[confirmation details]` | Message template fields in the WhatsApp bot |

Postgres nodes use generic schemas (`sms_schema`, `contact_schema`, `user_schema`, `email_collection_schema`, `voice_agent_user_schema`). Create your own with matching columns or adjust the queries.

The Wait node in the WhatsApp bot is set to `30`; choose the time unit you want (n8n defaults to hours).
