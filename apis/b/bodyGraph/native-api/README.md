# BodyGraph: Native API Reference

A consolidated summary of BodyGraph's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://bodygraph.com/docs/
- **API base URL:** `https://api.bodygraphchart.com`

## Authentication

### API Key

Connect with your Bodygraph API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bodygraph.com/hc-article/how-to-find-my-api-key/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Astrology Data](actions/generate-astrology-data.md) | `GET /v240815/astro-data` | [docs](https://bodygraph.com/docs/#generate-astrology-data) |
| [Generate HD Data](actions/generate-hd-data.md) | `GET /v221006/hd-data` | [docs](https://bodygraph.com/docs/#generate-hd-data) |
| [Search Locations](actions/search-locations.md) | `GET /v210502/locations` | [docs](https://bodygraph.com/docs/#find-timezone) |
