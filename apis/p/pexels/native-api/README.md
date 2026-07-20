# Pexels: Native API Reference

A consolidated summary of Pexels's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://www.pexels.com/api/documentation/
- **API base URL:** `https://api.pexels.com`

## Authentication

### API Key

Authenticate with a Pexels API key sent as the raw Authorization header value.

### Credentials

- **API Key:** `apiKey` · required · Pexels API key. MindCloud sends this value as the raw Authorization header through the shared REST header mapper.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.pexels.com/api/documentation/#authorization)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–80). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Photo](actions/get-photo.md) | `GET /v1/photos/:id` | [docs](https://www.pexels.com/api/documentation/#photos-show) |
| [Get Video](actions/get-video.md) | `GET /v1/videos/videos/:id` | [docs](https://www.pexels.com/api/documentation/#videos-show) |
| [List Collection Media](actions/list-collection-media.md) | `GET /v1/collections/:id` | [docs](https://www.pexels.com/api/documentation/#collections-media) |
| [List Curated Photos](actions/list-curated-photos.md) | `GET /v1/curated` | [docs](https://www.pexels.com/api/documentation/#photos-curated) |
| [List Featured Collections](actions/list-featured-collections.md) | `GET /v1/collections/featured` | [docs](https://www.pexels.com/api/documentation/#collections-featured) |
| [List My Collections](actions/list-my-collections.md) | `GET /v1/collections` | [docs](https://www.pexels.com/api/documentation/#collections-mine) |
| [List Popular Videos](actions/list-popular-videos.md) | `GET /v1/videos/popular` | [docs](https://www.pexels.com/api/documentation/#videos-popular) |
| [Search Photos](actions/search-photos.md) | `GET /v1/search` | [docs](https://www.pexels.com/api/documentation/#photos-search) |
| [Search Videos](actions/search-videos.md) | `GET /v1/videos/search` | [docs](https://www.pexels.com/api/documentation/#videos-search) |
