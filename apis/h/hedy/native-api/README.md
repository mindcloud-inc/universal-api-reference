# Hedy: Native API Reference

A consolidated summary of Hedy's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/
- **OpenAPI specification:** https://api.hedy.bot/v1/docs
- **API base URL:** `https://api.hedy.bot`

## Authentication

### API Key

Authenticate Hedy API requests with a bearer API key from Account Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.hedy.bot/en/articles/11663570-hedy-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Session Context](actions/create-session-context.md) | `POST https://api.hedy.bot/contexts` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Create Topic](actions/create-topic.md) | `POST https://api.hedy.bot/topics` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Create Webhook](actions/create-webhook.md) | `POST https://api.hedy.bot/webhooks` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Delete Session Context](actions/delete-session-context.md) | `DELETE https://api.hedy.bot/contexts/:contextId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Delete Topic](actions/delete-topic.md) | `DELETE https://api.hedy.bot/topics/:topicId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE https://api.hedy.bot/webhooks/:webhookId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Get Highlight Details](actions/get-highlight-details.md) | `GET https://api.hedy.bot/highlights/:highlightId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Get Session Context](actions/get-session-context.md) | `GET https://api.hedy.bot/contexts/:contextId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Get Session Details](actions/get-session-details.md) | `GET https://api.hedy.bot/sessions/:sessionId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Get Session To-Do Item](actions/get-session-to-do-item.md) | `GET https://api.hedy.bot/sessions/:sessionId/todos/:todoId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Get Topic Details](actions/get-topic-details.md) | `GET https://api.hedy.bot/topics/:topicId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Highlights](actions/list-highlights.md) | `GET https://api.hedy.bot/highlights` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Session Contexts](actions/list-session-contexts.md) | `GET https://api.hedy.bot/contexts` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Session Highlights](actions/list-session-highlights.md) | `GET https://api.hedy.bot/sessions/:sessionId/highlights` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Session To-Do Items](actions/list-session-to-do-items.md) | `GET https://api.hedy.bot/sessions/:sessionId/todos` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Sessions](actions/list-sessions.md) | `GET https://api.hedy.bot/sessions` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List To-Do Items](actions/list-to-do-items.md) | `GET https://api.hedy.bot/todos` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Topic Sessions](actions/list-topic-sessions.md) | `GET https://api.hedy.bot/topics/:topicId/sessions` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Topics](actions/list-topics.md) | `GET https://api.hedy.bot/topics` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [List Webhooks](actions/list-webhooks.md) | `GET https://api.hedy.bot/webhooks` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Update Session Context](actions/update-session-context.md) | `PATCH https://api.hedy.bot/contexts/:contextId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
| [Update Topic](actions/update-topic.md) | `PATCH https://api.hedy.bot/topics/:topicId` | [docs](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/) |
