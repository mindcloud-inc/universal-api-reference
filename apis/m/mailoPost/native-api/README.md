# MailoPost: Native API Reference

A consolidated summary of MailoPost's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://mailopost.ru/api.html
- **API base URL:** `https://api.mailopost.ru/v1`

## Authentication

### API Key

Use a MailoPost API token as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mailopost.ru/api.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `page_number`.

## Pagination

Use `page_size` in the query string to set the page size (default 25; accepted range 1–100). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | `POST /email/campaigns` | [docs](https://mailopost.ru/api.html) |
| [Create Email Template](actions/create-email-template.md) | `POST /email/templates` | [docs](https://mailopost.ru/api.html) |
| [Create Message Webhook](actions/create-message-webhook.md) | `POST /email/messages_webhooks` | [docs](https://mailopost.ru/api.html) |
| [Create Organization](actions/create-organization.md) | `POST /email/organizations` | [docs](https://mailopost.ru/api.html) |
| [Create Recipient](actions/create-recipient.md) | `POST /email/lists/:id/recipients` | [docs](https://mailopost.ru/api.html) |
| [Create Recipient List](actions/create-recipient-list.md) | `POST /email/lists` | [docs](https://mailopost.ru/api.html) |
| [Create Recipient List Parameter](actions/create-recipient-list-parameter.md) | `POST /email/lists/:id/parameters` | [docs](https://mailopost.ru/api.html) |
| [Delete Message Webhook](actions/delete-message-webhook.md) | `DELETE /email/messages_webhooks/:id` | [docs](https://mailopost.ru/api.html) |
| [Deliver Campaign](actions/deliver-campaign.md) | `PATCH /email/campaigns/:id/deliver` | [docs](https://mailopost.ru/api.html) |
| [Get Balance](actions/get-balance.md) | `GET /email/balance` | [docs](https://mailopost.ru/api.html) |
| [Get Campaign](actions/get-campaign.md) | `GET /email/campaigns/:id` | [docs](https://mailopost.ru/api.html) |
| [Get Current Organization](actions/get-current-organization.md) | `GET /email/organizations/current` | [docs](https://mailopost.ru/api.html) |
| [Get Email Message](actions/get-email-message.md) | `GET /email/messages/:id` | [docs](https://mailopost.ru/api.html) |
| [Get Email Template](actions/get-email-template.md) | `GET /email/templates/:template_id` | [docs](https://mailopost.ru/api.html) |
| [Get Message Webhook](actions/get-message-webhook.md) | `GET /email/messages_webhooks/:id` | [docs](https://mailopost.ru/api.html) |
| [Get Organization](actions/get-organization.md) | `GET /email/organizations/:id` | [docs](https://mailopost.ru/api.html) |
| [Get Recipient](actions/get-recipient.md) | `GET /email/lists/:list_id/recipients/:id` | [docs](https://mailopost.ru/api.html) |
| [Get Recipient List](actions/get-recipient-list.md) | `GET /email/lists/:id` | [docs](https://mailopost.ru/api.html) |
| [Import Recipients](actions/import-recipients.md) | `POST /email/lists/:id/recipients/imports` | [docs](https://mailopost.ru/api.html) |
| [List Campaigns](actions/list-campaigns.md) | `GET /email/campaigns` | [docs](https://mailopost.ru/api.html) |
| [List Email Templates](actions/list-email-templates.md) | `GET /email/templates` | [docs](https://mailopost.ru/api.html) |
| [List Message Webhooks](actions/list-message-webhooks.md) | `GET /email/messages_webhooks` | [docs](https://mailopost.ru/api.html) |
| [List Organizations](actions/list-organizations.md) | `GET /email/organizations` | [docs](https://mailopost.ru/api.html) |
| [List Recipient List Parameters](actions/list-recipient-list-parameters.md) | `GET /email/lists/:id/parameters` | [docs](https://mailopost.ru/api.html) |
| [List Recipient Lists](actions/list-recipient-lists.md) | `GET /email/lists` | [docs](https://mailopost.ru/api.html) |
| [List Recipients](actions/list-recipients.md) | `GET /email/lists/:id/recipients` | [docs](https://mailopost.ru/api.html) |
| [List Segments](actions/list-segments.md) | `GET /email/segments` | [docs](https://mailopost.ru/api.html) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /email/messages_webhooks/events` | [docs](https://mailopost.ru/api.html) |
| [List Webhook Message Kinds](actions/list-webhook-message-kinds.md) | `GET /email/messages_webhooks/kinds` | [docs](https://mailopost.ru/api.html) |
| [Schedule Campaign](actions/schedule-campaign.md) | `PATCH /email/campaigns/:id/schedule` | [docs](https://mailopost.ru/api.html) |
| [Search Recipients](actions/search-recipients.md) | `GET /email/recipients/search` | [docs](https://mailopost.ru/api.html) |
| [Send Email Message](actions/send-email-message.md) | `POST /email/messages` | [docs](https://mailopost.ru/api.html) |
| [Send Email Template Message](actions/send-email-template-message.md) | `POST /email/templates/:template_id/messages` | [docs](https://mailopost.ru/api.html) |
| [Set Current Organization](actions/set-current-organization.md) | `PATCH /email/organizations/:id/current` | [docs](https://mailopost.ru/api.html) |
| [Submit Email Template For Moderation](actions/submit-email-template-for-moderation.md) | `PATCH /email/templates/:template_id/to_pending` | [docs](https://mailopost.ru/api.html) |
| [Update Message Webhook](actions/update-message-webhook.md) | `PATCH /email/messages_webhooks/:id` | [docs](https://mailopost.ru/api.html) |
| [Update Organization](actions/update-organization.md) | `PATCH /email/organizations/:id` | [docs](https://mailopost.ru/api.html) |
| [Update Recipient](actions/update-recipient.md) | `PATCH /email/lists/:list_id/recipients/:id` | [docs](https://mailopost.ru/api.html) |
| [Update Recipient List](actions/update-recipient-list.md) | `PATCH /email/lists/:id` | [docs](https://mailopost.ru/api.html) |
| [Update Recipient List Parameter](actions/update-recipient-list-parameter.md) | `PATCH /email/lists/:list-id/parameters/:id` | [docs](https://mailopost.ru/api.html) |
