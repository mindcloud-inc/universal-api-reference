# Remindlo: Native API Reference

A consolidated summary of Remindlo's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://www.remindlo.co.uk/help/sms-reminder-api
- **API base URL:** `https://api.remindlo.co.uk/v1`

## Authentication

### API Key

Connect Remindlo with an API key from Dashboard > Settings > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.remindlo.co.uk/help/sms-reminder-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /webhooks/delete` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [Enroll Contact In Campaign](actions/enroll-contact-in-campaign.md) | `POST /campaigns-enroll` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [Send Message](actions/send-message.md) | `POST /messages` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
| [Upsert Contact](actions/upsert-contact.md) | `POST /contacts` | [docs](https://www.remindlo.co.uk/help/sms-reminder-api) |
