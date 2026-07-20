# Boomlify: Native API Reference

A consolidated summary of Boomlify's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://boomlify.com/en/temp-mail-api-docs
- **API base URL:** `https://v1.boomlify.com`

## Authentication

### API Key

Boomlify API key authentication. The official docs send the credential in the X-API-Key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://boomlify.com/en/temp-mail-api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Enable Dashboard Telegram Forwarding](actions/bulk-enable-dashboard-telegram-forwarding.md) | `POST /api/v1/emails/telegram-forwarding/bulk-enable` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=bulk-enable-dashboard-telegram-forwarding&tab=docs) |
| [Create Dashboard Email](actions/create-dashboard-email.md) | `POST /api/v1/emails/create` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=create-dashboard-email&tab=docs) |
| [Create Email](actions/create-email.md) | `POST /api/v1/emails/create` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=create-email&tab=docs) |
| [Delete Email](actions/delete-email.md) | `DELETE /api/v1/emails/{id}` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=delete-email&tab=docs) |
| [Get Account Credits](actions/get-account-credits.md) | `GET /api/v1/account/credits` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-account-credits&tab=docs) |
| [Get Account Info](actions/get-account-info.md) | `GET /api/v1/account/info` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-account-info&tab=docs) |
| [Get Account Usage](actions/get-account-usage.md) | `GET /api/v1/account/usage` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-usage&tab=docs) |
| [Get Dashboard Email](actions/get-dashboard-email.md) | `GET /api/v1/emails/{id}` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-dashboard-email&tab=docs) |
| [Get Dashboard Email Messages](actions/get-dashboard-email-messages.md) | `GET /api/v1/emails/{id}/messages` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-dashboard-messages&tab=docs) |
| [Get Dashboard Telegram Forwarding](actions/get-dashboard-telegram-forwarding.md) | `GET /api/v1/emails/{id}/telegram-forwarding` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-dashboard-telegram-forwarding&tab=docs) |
| [Get Email](actions/get-email.md) | `GET /api/v1/emails/{id}` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-email&tab=docs) |
| [Get Email Messages](actions/get-email-messages.md) | `GET /api/v1/emails/{id}/messages` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-messages&tab=docs) |
| [List Dashboard Emails](actions/list-dashboard-emails.md) | `GET /api/v1/emails` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=list-dashboard-emails&tab=docs) |
| [List Emails](actions/list-emails.md) | `GET /api/v1/emails` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=list-emails&tab=docs) |
| [Update Dashboard Telegram Forwarding](actions/update-dashboard-telegram-forwarding.md) | `POST /api/v1/emails/{id}/telegram-forwarding` | [docs](https://boomlify.com/en/temp-mail-api-docs?endpoint=update-dashboard-telegram-forwarding&tab=docs) |
