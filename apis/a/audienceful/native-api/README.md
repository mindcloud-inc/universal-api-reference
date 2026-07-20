# Audienceful: Native API Reference

A consolidated summary of Audienceful's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developer.audienceful.com/api-reference
- **API base URL:** `https://app.audienceful.com/api`

## Authentication

### API Key Primary

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developer.audienceful.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`. The next-page cursor is read from `next`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 500 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | `POST /people/fields/` | [docs](https://developer.audienceful.com/api-reference/fields/create) |
| [Create Person](actions/create-person.md) | `POST /people/` | [docs](https://developer.audienceful.com/api-reference/people/create) |
| [Delete Field](actions/delete-field.md) | `DELETE /people/fields/{{id}}/` | [docs](https://developer.audienceful.com/api-reference/fields/delete) |
| [Delete Person](actions/delete-person.md) | `DELETE /people/` | [docs](https://developer.audienceful.com/api-reference/people/delete) |
| [List Fields](actions/list-fields.md) | `GET /people/fields/` | [docs](https://developer.audienceful.com/api-reference/fields/get) |
| [List People](actions/list-people.md) | `GET /people/` | [docs](https://developer.audienceful.com/api-reference/people/get) |
| [List Send Reports](actions/list-send-reports.md) | `GET /emails/reports` | [docs](https://developer.audienceful.com/api-reference/sendReports/get) |
| [Trigger Event](actions/trigger-event.md) | `POST /automations/event/` | [docs](https://developer.audienceful.com/api-reference/automations/event) |
| [Update Person](actions/update-person.md) | `PATCH /people/` | [docs](https://developer.audienceful.com/api-reference/people/update) |
