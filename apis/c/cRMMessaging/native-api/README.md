# CRM Messaging: Native API Reference

A consolidated summary of CRM Messaging's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://crm-messaging.cloud/docs-category/api-documentation/
- **API base URL:** `https://app.crm-messaging.cloud`

## Authentication

### API Token

Authenticate CRM Messaging API requests with a bearer token from the Developer Console.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://crm-messaging.cloud/docs/setup-sms-api-account/)

## API conventions

Response data is read from `data.messages`. The current page number is read from `data.page`.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /index.php/Api/createContact` | [docs](https://crm-messaging.cloud/docs/create-contact/) |
| [Delete Contact](actions/delete-contact.md) | `POST /index.php/Api/deleteContact` | [docs](https://crm-messaging.cloud/docs/delete-contact-crm-messaging-api/) |
| [List Messages](actions/list-messages.md) | `GET /index.php/Api/messageHistory` | [docs](https://crm-messaging.cloud/docs/message-history-api/) |
| [Make Voice Call](actions/make-voice-call.md) | `POST https://campaigns.crm-messaging.cloud/api/voice-call` | [docs](https://crm-messaging.cloud/docs/make-voice-calls-by-api/) |
| [Send SMS](actions/send-sms.md) | `POST /index.php/Api/sendMsg` | [docs](https://crm-messaging.cloud/docs/send-sms/) |
| [Send WhatsApp Template](actions/send-whats-app-template.md) | `POST /index.php/Api/sendMsg` | [docs](https://crm-messaging.cloud/docs/send-whatsapp-templates/) |
| [Update Contact](actions/update-contact.md) | `POST /index.php/Api/updateContact` | [docs](https://crm-messaging.cloud/docs/update-contact/) |
