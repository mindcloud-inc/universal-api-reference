# Autom: Native API Reference

A consolidated summary of Autom's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.autom.dev/
- **API base URL:** `https://api.autom.dev`

## Authentication

### Header API Key

Authenticate with an Autom API key sent only in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Autom API key used for the x-api-key request header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.autom.dev/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://docs.autom.dev/usage) |
| [Search Bing](actions/search-bing.md) | `GET /v1/bing/search` | [docs](https://docs.autom.dev/bing-search) |
| [Search Brave](actions/search-brave.md) | `GET /v1/brave/search` | [docs](https://docs.autom.dev/brave-search) |
| [Search Google](actions/search-google.md) | `GET /v1/google/search` | [docs](https://docs.autom.dev/google-search) |
| [Search Google Autocomplete Suggestions](actions/search-google-autocomplete-suggestions.md) | `GET /v1/google/search/autocomplete` | [docs](https://docs.autom.dev/google-search-autocomplete) |
| [Search Google Images](actions/search-google-images.md) | `GET /v1/google/images` | [docs](https://docs.autom.dev/google-images) |
| [Search Google News](actions/search-google-news.md) | `GET /v1/google/news` | [docs](https://docs.autom.dev/google-news) |
| [Search Google Videos](actions/search-google-videos.md) | `GET /v1/google/videos` | [docs](https://docs.autom.dev/google-videos) |
