# AskHandle: Native API Reference

A consolidated summary of AskHandle's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://dashboard.askhandle.com/api/v1/docs/api_reference.html
- **API base URL:** `https://dashboard.askhandle.com/api/v1`

## Authentication

### API Key

Use your AskHandle API key to authorize REST API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#authentication)

## API conventions

Response data is read from `results`. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (default 20). Use `offset` in the query string as the record offset.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | `POST /messages/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#message) |
| [Create Room](actions/create-room.md) | `POST /rooms/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:uuid/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook) |
| [List Keyword Notifications](actions/list-keyword-notifications.md) | `GET /keyword_notifications/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#keyword-notification) |
| [List Leads](actions/list-leads.md) | `GET /leads/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#lead) |
| [List Messages](actions/list-messages.md) | `GET /messages/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#message) |
| [List Rooms](actions/list-rooms.md) | `GET /rooms/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook) |
| [Retrieve Message](actions/retrieve-message.md) | `GET /messages/:uuid/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#message) |
| [Retrieve Room](actions/retrieve-room.md) | `GET /rooms/:label/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room) |
| [Retrieve Webhook](actions/retrieve-webhook.md) | `GET /webhooks/:uuid/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook) |
| [Update Room](actions/update-room.md) | `PUT /rooms/:label/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room) |
| [Update Room Field](actions/update-room-field.md) | `PATCH /rooms/:label/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:uuid/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook) |
| [Update Webhook Field](actions/update-webhook-field.md) | `PATCH /webhooks/:uuid/` | [docs](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook) |
