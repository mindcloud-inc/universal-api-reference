# Pipefile: Native API Reference

A consolidated summary of Pipefile's API configuration and 7 documented operations.

- **API base URL:** `https://api.pipefile.com/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.pipefile.com/v1/contacts/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`. The total page count is read from `num_pages`.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path |
| --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts/` |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/` |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id/` |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id/` |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/` |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/` |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:id/` |
