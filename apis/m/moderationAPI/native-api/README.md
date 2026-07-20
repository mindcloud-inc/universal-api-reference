# Moderation API: Native API Reference

A consolidated summary of Moderation API's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://docs.moderationapi.com/
- **OpenAPI specification:** https://api.moderationapi.com/v1/openapi.json
- **API base URL:** `https://api.moderationapi.com/v1`

## Authentication

### API Key

Authenticate requests with a Moderation API secret key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.moderationapi.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Words To Wordlist](actions/add-words-to-wordlist.md) | `POST /wordlist/:id/words` | [docs](https://docs.moderationapi.com/api-reference/wordlist/add-words-to-wordlist) |
| [Analyze Audio](actions/analyze-audio.md) | `POST /moderate/audio` | [docs](https://docs.moderationapi.com/api-reference/moderate/analyze-audio) |
| [Analyze Image](actions/analyze-image.md) | `POST /moderate/image` | [docs](https://docs.moderationapi.com/api-reference/moderate/analyze-image) |
| [Analyze Object](actions/analyze-object.md) | `POST /moderate/object` | [docs](https://docs.moderationapi.com/api-reference/moderate/analyze-object) |
| [Analyze Text](actions/analyze-text.md) | `POST /moderate/text` | [docs](https://docs.moderationapi.com/api-reference/moderate/analyze-text) |
| [Analyze Video](actions/analyze-video.md) | `POST /moderate/video` | [docs](https://docs.moderationapi.com/api-reference/moderate/analyze-video) |
| [Create A New Author](actions/create-a-new-author.md) | `POST /authors` | [docs](https://docs.moderationapi.com/api-reference/author/create-a-new-author) |
| [Create An Action](actions/create-an-action.md) | `POST /actions` | [docs](https://docs.moderationapi.com/api-reference/actions/create-an-action) |
| [Delete An Action](actions/delete-an-action.md) | `DELETE /actions/:id` | [docs](https://docs.moderationapi.com/api-reference/actions/delete-an-action) |
| [Delete An Author](actions/delete-an-author.md) | `DELETE /authors/:id` | [docs](https://docs.moderationapi.com/api-reference/author/delete-an-author) |
| [Execute Moderation Action](actions/execute-moderation-action.md) | `POST /actions/execute` | [docs](https://docs.moderationapi.com/api-reference/actions/execute-moderation-action) |
| [Get A Queue](actions/get-a-queue.md) | `GET /queue/:id` | [docs](https://docs.moderationapi.com/api-reference/review-queues/get-a-queue) |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://docs.moderationapi.com/api-reference/account/get-account-details) |
| [Get An Action](actions/get-an-action.md) | `GET /actions/:id` | [docs](https://docs.moderationapi.com/api-reference/actions/get-an-action) |
| [Get Author Details](actions/get-author-details.md) | `GET /authors/:id` | [docs](https://docs.moderationapi.com/api-reference/author/get-author-details) |
| [Get Embedding Status](actions/get-embedding-status.md) | `GET /wordlist/:id/embedding-status` | [docs](https://docs.moderationapi.com/api-reference/wordlist/get-embedding-status) |
| [Get Queue Items](actions/get-queue-items.md) | `GET /queue/:id/items` | [docs](https://docs.moderationapi.com/api-reference/review-queues/get-queue-items) |
| [Get Queue Statistics](actions/get-queue-statistics.md) | `GET /queue/:id/stats` | [docs](https://docs.moderationapi.com/api-reference/review-queues/get-queue-statistics) |
| [Get Wordlist](actions/get-wordlist.md) | `GET /wordlist/:id` | [docs](https://docs.moderationapi.com/api-reference/wordlist/get-wordlist) |
| [List Authors](actions/list-authors.md) | `GET /authors` | [docs](https://docs.moderationapi.com/api-reference/author/list-authors) |
| [List Moderation Actions](actions/list-moderation-actions.md) | `GET /actions` | [docs](https://docs.moderationapi.com/api-reference/actions/list-moderation-actions) |
| [List Wordlists](actions/list-wordlists.md) | `GET /wordlist` | [docs](https://docs.moderationapi.com/api-reference/wordlist/list-wordlists) |
| [Remove Words From Wordlist](actions/remove-words-from-wordlist.md) | `DELETE /wordlist/:id/words` | [docs](https://docs.moderationapi.com/api-reference/wordlist/remove-words-from-wordlist) |
| [Resolve A Queue Item](actions/resolve-a-queue-item.md) | `POST /queue/:id/items/:itemId/resolve` | [docs](https://docs.moderationapi.com/api-reference/review-queues/resolve-a-queue-item) |
| [Submit Content For Moderation](actions/submit-content-for-moderation.md) | `POST /moderate` | [docs](https://docs.moderationapi.com/content-moderation/submit-content) |
| [Unresolve A Queue Item](actions/unresolve-a-queue-item.md) | `POST /queue/:id/items/:itemId/unresolve` | [docs](https://docs.moderationapi.com/api-reference/review-queues/unresolve-a-queue-item) |
| [Update An Action](actions/update-an-action.md) | `PUT /actions/:id` | [docs](https://docs.moderationapi.com/api-reference/actions/update-an-action) |
| [Update Author Details](actions/update-author-details.md) | `PUT /authors/:id` | [docs](https://docs.moderationapi.com/api-reference/author/update-author-details) |
| [Update Wordlist](actions/update-wordlist.md) | `PUT /wordlist/:id` | [docs](https://docs.moderationapi.com/api-reference/wordlist/update-wordlist) |
