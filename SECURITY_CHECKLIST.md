# Security Checklist

Use this checklist before publishing or updating the workflow.

## Removed from this template

- Real GOWA credential ID and credential name
- Real OpenAI credential ID and credential name
- Real webhook path and webhook ID
- Real GOWA server domain
- Real admin WhatsApp numbers
- Real payment account numbers
- Real DataTable ID and project ID
- Real n8n instance ID

## Recommended before public release

- Rotate any credential that may have been exposed before sanitization.
- Do not commit `.env` files.
- Keep real payment data and private customer service rules outside the public workflow.
- Use placeholders and environment variables for production values.
