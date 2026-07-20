# ScrapeOwl: Native API Reference

A consolidated summary of ScrapeOwl's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://scrapeowl.com/docs/
- **API base URL:** `https://api.scrapeowl.com/v1`

## Authentication

### API Key

ScrapeOwl API key from the dashboard. The key is sent as api_key in action requests per ScrapeOwl docs.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://scrapeowl.com/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://scrapeowl.com/docs/) |
| [Scrape URL](actions/scrape-url.md) | `POST /scrape` | [docs](https://scrapeowl.com/docs/) |
