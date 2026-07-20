# Livestorm: Native API Reference

A consolidated summary of Livestorm's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.livestorm.co/reference
- **OpenAPI specification:** https://api.livestorm.co/api-docs/v1/swagger.yaml
- **API base URL:** `https://api.livestorm.co/v1`

## Authentication

### API Key

Use a Livestorm Public API token. Livestorm requires a validated workspace with Public API access enabled before tokens can be generated.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://developers.livestorm.co/docs/api-token-authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.page_count`. The current page number is read from `meta.current_page`.

## Pagination

Use `page[size]` in the query string to set the page size. Use `page[number]` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Event Tag](actions/assign-event-tag.md) | `POST events/:id/tags` | [docs](https://developers.livestorm.co/reference/post_events-id-tags) |
| [Bulk Register Session People](actions/bulk-register-session-people.md) | `POST sessions/:id/people/bulk` | [docs](https://developers.livestorm.co/reference/post_sessions-id-people-bulk) |
| [Create Event](actions/create-event.md) | `POST events` | [docs](https://developers.livestorm.co/reference/post_events) |
| [Create Event Session](actions/create-event-session.md) | `POST events/:id/sessions` | [docs](https://developers.livestorm.co/reference/post_events-id-sessions) |
| [Create Webhook](actions/create-webhook.md) | `POST webhooks` | [docs](https://developers.livestorm.co/reference/post_webhooks) |
| [Delete Event](actions/delete-event.md) | `DELETE events/:id` | [docs](https://developers.livestorm.co/reference/delete_events-id) |
| [Delete Session](actions/delete-session.md) | `DELETE sessions/:id` | [docs](https://developers.livestorm.co/reference/delete_sessions-id) |
| [Delete Session Person](actions/delete-session-person.md) | `DELETE sessions/:id/people/:peopleId` | [docs](https://developers.livestorm.co/reference/delete_sessions-id-people-people-id) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE webhooks/:id` | [docs](https://developers.livestorm.co/reference/delete_webhooks-id) |
| [Get Event](actions/get-event.md) | `GET events/:id` | [docs](https://developers.livestorm.co/reference/get_events-id) |
| [Get Event Person](actions/get-event-person.md) | `GET events/:eventId/people/:id` | [docs](https://developers.livestorm.co/reference/get_events-event-id-people-id) |
| [Get Job](actions/get-job.md) | `GET jobs/:id` | [docs](https://developers.livestorm.co/reference/get_jobs-id) |
| [Get Person](actions/get-person.md) | `GET people/:id` | [docs](https://developers.livestorm.co/reference/get_people-id) |
| [Get Session](actions/get-session.md) | `GET sessions/:id` | [docs](https://developers.livestorm.co/reference/get_sessions-id) |
| [Get Session Person](actions/get-session-person.md) | `GET sessions/:sessionId/people/:id` | [docs](https://developers.livestorm.co/reference/get_sessions-session-id-people-id) |
| [List Event People](actions/list-event-people.md) | `GET events/:id/people` | [docs](https://developers.livestorm.co/reference/get_events-id-people) |
| [List Event Sessions](actions/list-event-sessions.md) | `GET events/:id/sessions` | [docs](https://developers.livestorm.co/reference/get_events-id-sessions) |
| [List Events](actions/list-events.md) | `GET events` | [docs](https://developers.livestorm.co/reference/get_events) |
| [List People](actions/list-people.md) | `GET people` | [docs](https://developers.livestorm.co/reference/get_people) |
| [List People Attributes](actions/list-people-attributes.md) | `GET people_attributes` | [docs](https://developers.livestorm.co/reference/get_people-attributes) |
| [List Session People](actions/list-session-people.md) | `GET sessions/:id/people` | [docs](https://developers.livestorm.co/reference/get_sessions-id-people) |
| [List Session Questions](actions/list-session-questions.md) | `GET sessions/:id/questions` | [docs](https://developers.livestorm.co/reference/get_sessions-id-questions) |
| [List Session Recordings](actions/list-session-recordings.md) | `GET sessions/:id/recordings` | [docs](https://developers.livestorm.co/reference/get_sessions-id-recordings) |
| [List Sessions](actions/list-sessions.md) | `GET sessions` | [docs](https://developers.livestorm.co/reference/get_sessions) |
| [List Webhooks](actions/list-webhooks.md) | `GET webhooks` | [docs](https://developers.livestorm.co/reference/get_webhooks) |
| [Register Session Person](actions/register-session-person.md) | `POST sessions/:id/people` | [docs](https://developers.livestorm.co/reference/post_sessions-id-people) |
| [Remove Event Tag](actions/remove-event-tag.md) | `DELETE events/:id/tags` | [docs](https://developers.livestorm.co/reference/delete_events-id-tags) |
| [Test Authentication](actions/test-authentication.md) | `GET ping` | [docs](https://developers.livestorm.co/reference/get_ping) |
| [Update Event](actions/update-event.md) | `PATCH events/:id` | [docs](https://developers.livestorm.co/reference/patch_events-id) |
| [Update Session](actions/update-session.md) | `PATCH sessions/:id` | [docs](https://developers.livestorm.co/reference/patch_sessions-id) |
