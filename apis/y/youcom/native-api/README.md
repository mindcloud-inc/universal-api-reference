# You.com: Native API Reference

A consolidated summary of You.com's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.you.com/welcome
- **API base URL:** `https://api.you.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.you.com/administration/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask Advanced Agent](actions/ask-advanced-agent.md) | `POST /v1/agents/runs` | [docs](https://docs.you.com/custom-solutions/agents/advanced-agent/advanced-agent-runs) |
| [Ask Express Agent](actions/ask-express-agent.md) | `POST /v1/agents/runs` | [docs](https://docs.you.com/custom-solutions/agents/express-agent/express-agent-runs) |
| [Get Contents](actions/get-contents.md) | `POST https://ydc-index.io/v1/contents` | [docs](https://docs.you.com/api-reference/contents) |
| [Get Live News](actions/get-live-news.md) | `GET https://api.ydc-index.io/livenews` | [docs](https://docs.you.com/custom-solutions/live-news/live-news) |
| [Research](actions/research.md) | `POST /v1/research` | [docs](https://docs.you.com/api-reference/research/v1-research) |
| [Search](actions/search.md) | `GET https://ydc-index.io/v1/search` | [docs](https://docs.you.com/api-reference/search/v1-search) |
| [Search Images](actions/search-images.md) | `GET https://image-search.ydc-index.io/images` | [docs](https://docs.you.com/custom-solutions/images/images) |
