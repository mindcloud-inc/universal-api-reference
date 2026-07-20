# Columns AI: Native API Reference

A consolidated summary of Columns AI's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://github.com/varchar-io/vaas
- **API base URL:** `https://columns.ai/api`

## Authentication

### API Key

Connect with a Columns AI API key from the profile page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/varchar-io/vaas)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Graph Image](actions/download-graph-image.md) | `GET /sdk/image/:id` | [docs](https://github.com/varchar-io/vaas/blob/main/src/index.ts#L310-L329) |
| [Get Visual Template](actions/get-visual-template.md) | `POST /snapshot/visual` | [docs](https://github.com/varchar-io/vaas/blob/main/src/index.ts#L238-L252) |
| [Publish Graph](actions/publish-graph.md) | `POST /sdk/graph` | [docs](https://github.com/varchar-io/vaas/blob/main/src/index.ts#L277-L300) |
