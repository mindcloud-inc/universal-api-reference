# Loops: Native API Reference

A consolidated summary of Loops's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://loops.so/docs/api-reference/intro
- **OpenAPI specification:** https://app.loops.so/openapi.json
- **API base URL:** `https://app.loops.so/api/v1`

## Authentication

### API Key

Use a Loops API key from Settings -> API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://loops.so/docs/api-reference/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.nextCursor`. The total page count is read from `pagination.totalPages`.

## Pagination

Use `perPage` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Contact Suppression](actions/check-contact-suppression.md) | `GET /contacts/suppression` | [docs](https://loops.so/docs/api-reference/check-contact-suppression) |
| [Create Contact](actions/create-contact.md) | `POST /contacts/create` | [docs](https://loops.so/docs/api-reference/create-contact) |
| [Create Contact Property](actions/create-contact-property.md) | `POST /contacts/properties` | [docs](https://loops.so/docs/api-reference/create-contact-property) |
| [Delete Contact](actions/delete-contact.md) | `POST /contacts/delete` | [docs](https://loops.so/docs/api-reference/delete-contact) |
| [Find Contact](actions/find-contact.md) | `GET /contacts/find` | [docs](https://loops.so/docs/api-reference/find-contact) |
| [List Contact Properties](actions/list-contact-properties.md) | `GET /contacts/properties` | [docs](https://loops.so/docs/api-reference/list-contact-properties) |
| [List Dedicated Sending IP Addresses](actions/list-dedicated-sending-ip-addresses.md) | `GET /dedicated-sending-ips` | [docs](https://loops.so/docs/api-reference/dedicated-sending-ips) |
| [List Mailing Lists](actions/list-mailing-lists.md) | `GET /lists` | [docs](https://loops.so/docs/api-reference/list-mailing-lists) |
| [List Transactional Emails](actions/list-transactional-emails.md) | `GET /transactional` | [docs](https://loops.so/docs/api-reference/list-transactional-emails) |
| [Remove Contact Suppression](actions/remove-contact-suppression.md) | `DELETE /contacts/suppression` | [docs](https://loops.so/docs/api-reference/remove-contact-suppression) |
| [Send Event](actions/send-event.md) | `POST /events/send` | [docs](https://loops.so/docs/api-reference/send-event) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /transactional` | [docs](https://loops.so/docs/api-reference/send-transactional-email) |
| [Test API Key](actions/test-api-key.md) | `GET /api-key` | [docs](https://loops.so/docs/api-reference/api-key) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/update` | [docs](https://loops.so/docs/api-reference/update-contact) |
