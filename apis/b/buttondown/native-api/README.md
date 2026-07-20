# Buttondown: Native API Reference

A consolidated summary of Buttondown's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.buttondown.com/api-introduction
- **API base URL:** `https://api.buttondown.com/v1`

## Authentication

### API Key

Connect Buttondown with an API key from Buttondown Settings > API > Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.buttondown.com/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Draft Email](actions/create-draft-email.md) | `POST /emails` | [docs](https://docs.buttondown.com/api-emails-create) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /subscribers` | [docs](https://docs.buttondown.com/api-subscribers-create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.buttondown.com/api-webhooks-create) |
| [Delete Email](actions/delete-email.md) | `DELETE /emails/:id` | [docs](https://docs.buttondown.com/api-emails-delete) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:id_or_email` | [docs](https://docs.buttondown.com/api-subscribers-delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://docs.buttondown.com/api-webhooks-delete) |
| [List Emails](actions/list-emails.md) | `GET /emails` | [docs](https://docs.buttondown.com/api-emails-list) |
| [List Newsletters](actions/list-newsletters.md) | `GET /newsletters` | [docs](https://docs.buttondown.com/api-newsletters-list) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://docs.buttondown.com/api-subscribers-list) |
| [List Webhook Attempts](actions/list-webhook-attempts.md) | `GET /webhooks/:id/attempts` | [docs](https://docs.buttondown.com/api-webhooks-attempts-list) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.buttondown.com/api-webhooks-list) |
| [Retrieve Email](actions/retrieve-email.md) | `GET /emails/:id` | [docs](https://docs.buttondown.com/api-emails-retrieve) |
| [Retrieve Subscriber](actions/retrieve-subscriber.md) | `GET /subscribers/:id_or_email` | [docs](https://docs.buttondown.com/api-subscribers-retrieve) |
| [Retrieve Webhook](actions/retrieve-webhook.md) | `GET /webhooks/:id` | [docs](https://docs.buttondown.com/api-webhooks-retrieve) |
| [Send Draft Email](actions/send-draft-email.md) | `POST /emails/:id/send-draft` | [docs](https://docs.buttondown.com/api-emails-send-draft) |
| [Test Webhook](actions/test-webhook.md) | `POST /webhooks/:id/test` | [docs](https://docs.buttondown.com/api-webhooks-test) |
| [Update Draft Email](actions/update-draft-email.md) | `PATCH /emails/:id` | [docs](https://docs.buttondown.com/api-emails-update) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /subscribers/:id_or_email` | [docs](https://docs.buttondown.com/api-subscribers-update) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:id` | [docs](https://docs.buttondown.com/api-webhooks-update) |
