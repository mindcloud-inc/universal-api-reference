# Tavily: Native API Reference

A consolidated summary of Tavily's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.tavily.com/documentation/api-reference/introduction
- **API base URL:** `https://api.tavily.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.tavily.com/documentation/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Crawl Site](actions/crawl-site.md) | `POST /crawl` | [docs](https://docs.tavily.com/documentation/api-reference/endpoint/crawl) |
| [Create Research Task](actions/create-research-task.md) | `POST /research` | [docs](https://docs.tavily.com/documentation/api-reference/endpoint/research) |
| [Extract Content](actions/extract-content.md) | `POST /extract` | [docs](https://docs.tavily.com/documentation/api-reference/endpoint/extract) |
| [Get Research Task Status](actions/get-research-task-status.md) | `GET /research/:request_id` | [docs](https://docs.tavily.com/documentation/api-reference/endpoint/research-get) |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://docs.tavily.com/documentation/api-reference/endpoint/usage) |
| [Map Site](actions/map-site.md) | `POST /map` | [docs](https://docs.tavily.com/documentation/api-reference/endpoint/map) |
| [Search Web](actions/search-web.md) | `POST /search` | [docs](https://docs.tavily.com/documentation/api-reference/endpoint/search) |
