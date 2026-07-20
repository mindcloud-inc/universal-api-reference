# SMASHSEND Email Marketing: Native API Reference

A consolidated summary of SMASHSEND Email Marketing's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://smashsend.com/docs
- **API base URL:** `https://api.smashsend.com`

## Authentication

### API Key

Use a SMASHSEND API key with bearer authorization.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://smashsend.com/docs/api/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact Property](actions/create-contact-property.md) | `POST /v1/contact-properties` | [docs](https://smashsend.com/docs/api/contact-properties) |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /v1/contacts` | [docs](https://smashsend.com/docs/api/contacts) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://smashsend.com/docs/api/webhooks) |
| [Delete Contact By Email](actions/delete-contact-by-email.md) | `DELETE /v1/contacts/by-email/:email` | [docs](https://smashsend.com/docs/api/contacts) |
| [Delete Contact Property](actions/delete-contact-property.md) | `DELETE /v1/contact-properties/:propertyId` | [docs](https://smashsend.com/docs/api/contact-properties) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/:webhookId` | [docs](https://smashsend.com/docs/api/webhooks) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/:contactId` | [docs](https://smashsend.com/docs/api/contacts) |
| [Get Contact Property](actions/get-contact-property.md) | `GET /v1/contact-properties/:propertyId` | [docs](https://smashsend.com/docs/api/contact-properties) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/:webhookId` | [docs](https://smashsend.com/docs/api/webhooks) |
| [List Contact Properties](actions/list-contact-properties.md) | `GET /v1/contact-properties` | [docs](https://smashsend.com/docs/api/contact-properties) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://smashsend.com/docs/api/contacts) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://smashsend.com/docs/api/webhooks) |
| [Search Contacts](actions/search-contacts.md) | `GET /v1/contacts/search` | [docs](https://smashsend.com/docs/api/contacts) |
| [Track Event](actions/track-event.md) | `POST /v1/events` | [docs](https://smashsend.com/docs/api/events) |
| [Track Events Batch](actions/track-events-batch.md) | `POST /v1/events/batch` | [docs](https://smashsend.com/docs/api/events) |
| [Update Contact Property](actions/update-contact-property.md) | `POST /v1/contact-properties/:propertyId` | [docs](https://smashsend.com/docs/api/contact-properties) |
| [Update Webhook](actions/update-webhook.md) | `POST /v1/webhooks/:webhookId` | [docs](https://smashsend.com/docs/api/webhooks) |
| [Validate API Key](actions/validate-api-key.md) | `GET /v1/api-keys/check` | [docs](https://smashsend.com/docs/api/api-keys) |
