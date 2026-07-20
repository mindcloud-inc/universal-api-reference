# Datelist: Native API Reference

A consolidated summary of Datelist's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://apidoc.datelist.io/
- **API base URL:** `https://datelist.io/api`

## Authentication

### API Key

Use your Datelist API key. Datelist documents bearer-token authentication in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidoc.datelist.io/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://apidoc.datelist.io/webhooks) |
| [Delete Booked Slot](actions/delete-booked-slot.md) | `DELETE /booked_slots/:id` | [docs](https://apidoc.datelist.io/booked_slots) |
| [List Booked Slots](actions/list-booked-slots.md) | `GET /booked_slots` | [docs](https://apidoc.datelist.io/booked_slots) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars` | [docs](https://apidoc.datelist.io/calendars) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://apidoc.datelist.io/products) |
| [Update Booked Slot](actions/update-booked-slot.md) | `PATCH /booked_slots/:id` | [docs](https://apidoc.datelist.io/booked_slots) |
