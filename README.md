# n8n GOWA AI WhatsApp Customer Service Chatbot

Open-source n8n workflow template for building an AI-powered WhatsApp customer service chatbot using GOWA WhatsApp API, OpenAI, n8n Agent, memory, image analysis, and order status tracking.

> This repository contains a sanitized public template. No API keys, credentials, private webhook URL, phone numbers, bank account numbers, or private instance IDs are included.

## Features

- WhatsApp incoming message webhook
- Ignore group messages
- Admin/human sender filter
- Mark message as read
- Typing indicator
- Text message handling
- Image message handling
- Image analysis with OpenAI vision model
- AI Agent customer service flow
- Memory per WhatsApp number
- Order status tracking with n8n DataTable
- Send WhatsApp reply through GOWA

## Workflow Overview

```text
WhatsApp Webhook
  ↓
Filter admin / group messages
  ↓
Detect text or image message
  ↓
Read message + typing indicator
  ↓
Analyze image when needed
  ↓
Format final input
  ↓
AI Agent + Memory + DataTable tools
  ↓
Send WhatsApp reply
```

## Requirements

- n8n
- GOWA WhatsApp API node
- OpenAI credential in n8n
- GOWA credential in n8n
- n8n DataTable with at least these columns:
  - `whatsapp`
  - `status`

## Setup

1. Import the workflow JSON from:

```text
workflows/n8n-gowa-ai-chatbot-sanitized.json
```

2. Reconnect credentials in n8n:
   - OpenAI credential
   - GOWA WhatsApp API credential

3. Replace placeholders:
   - `REPLACE_WITH_YOUR_WEBHOOK_PATH`
   - `REPLACE_WITH_YOUR_WEBHOOK_ID`
   - `REPLACE_WITH_YOUR_DATATABLE_ID`
   - `YOUR_PROJECT_ID`
   - `ADMIN_WHATSAPP_1`
   - `ADMIN_WHATSAPP_2`
   - `ADMIN_WHATSAPP_3`
   - `YOUR_BANK_ACCOUNT_NUMBER`
   - `YOUR_ACCOUNT_NAME`
   - `YOUR_DANA_NUMBER`
   - `@your_social_media`

4. Set environment variable for GOWA base URL:

```env
GOWA_BASE_URL=https://your-gowa-domain.com
```

5. Adjust the system prompt to match your business, pricing, payment method, and customer service rules.

## Important Security Notes

Before making changes public, always check that your workflow does not contain:

- API keys
- Credential IDs from your production n8n
- Real webhook URL
- Real phone numbers
- Real payment data
- Private server domain
- Database IDs
- Instance IDs

## License

MIT
