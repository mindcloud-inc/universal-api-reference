# SerpApi: Native API Reference

A consolidated summary of SerpApi's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://serpapi.com/search-engine-apis
- **API base URL:** `https://serpapi.com`

## Authentication

### API Key

Use your SerpApi private API key. SerpApi expects the key as the shared `api_key` query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://serpapi.com/account-api)

## API conventions

Responses from this API use JSON. Response data is read from `organic_results`. The current page number is read from `serpapi_pagination.current`.

## Pagination

Use `num` in the query string to set the page size (default 10; accepted range 1–10). Use `start` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Google](actions/autocomplete-google.md) | `GET /search.json` | [docs](https://serpapi.com/google-autocomplete-api) |
| [Search Bing Images](actions/search-bing-images.md) | `GET /search.json` | [docs](https://serpapi.com/bing-images-api) |
| [Search Bing Web](actions/search-bing-web.md) | `GET /search.json` | [docs](https://serpapi.com/bing-search-api) |
| [Search DuckDuckGo Light](actions/search-duckduckgo-light.md) | `GET /search.json` | [docs](https://serpapi.com/duckduckgo-light-api) |
| [Search DuckDuckGo Web](actions/search-duckduckgo-web.md) | `GET /search.json` | [docs](https://serpapi.com/duckduckgo-search-api) |
| [Search Google](actions/search-google.md) | `GET /search.json` | [docs](https://serpapi.com/search-api) |
| [Search Google AI Mode](actions/search-google-ai-mode.md) | `GET /search.json` | [docs](https://serpapi.com/google-ai-mode-api) |
| [Search Google AI Overview](actions/search-google-ai-overview.md) | `GET /search.json` | [docs](https://serpapi.com/google-ai-overview-api) |
| [Search Google Events](actions/search-google-events.md) | `GET /search.json` | [docs](https://serpapi.com/google-events-api) |
| [Search Google Finance](actions/search-google-finance.md) | `GET /search.json` | [docs](https://serpapi.com/google-finance-api) |
| [Search Google Forums](actions/search-google-forums.md) | `GET /search.json` | [docs](https://serpapi.com/google-forums-api) |
| [Search Google Images](actions/search-google-images.md) | `GET /search.json` | [docs](https://serpapi.com/google-images-api) |
| [Search Google Jobs](actions/search-google-jobs.md) | `GET /search.json` | [docs](https://serpapi.com/google-jobs-api) |
| [Search Google Light](actions/search-google-light.md) | `GET /search.json` | [docs](https://serpapi.com/google-light-api) |
| [Search Google Local](actions/search-google-local.md) | `GET /search.json` | [docs](https://serpapi.com/google-local-api) |
| [Search Google Maps](actions/search-google-maps.md) | `GET /search.json` | [docs](https://serpapi.com/google-maps-api) |
| [Search Google News](actions/search-google-news.md) | `GET /search.json` | [docs](https://serpapi.com/google-news-api) |
| [Search Google Patents](actions/search-google-patents.md) | `GET /search.json` | [docs](https://serpapi.com/google-patents-api) |
| [Search Google Scholar](actions/search-google-scholar.md) | `GET /search.json` | [docs](https://serpapi.com/google-scholar-api) |
| [Search Google Shopping](actions/search-google-shopping.md) | `GET /search.json` | [docs](https://serpapi.com/google-shopping-api) |
| [Search Google Trends](actions/search-google-trends.md) | `GET /search.json` | [docs](https://serpapi.com/google-trends-api) |
| [Search Google Videos](actions/search-google-videos.md) | `GET /search.json` | [docs](https://serpapi.com/google-videos-api) |
| [Search Yahoo Web](actions/search-yahoo-web.md) | `GET /search.json` | [docs](https://serpapi.com/yahoo-search-api) |
| [Search YouTube](actions/search-youtube.md) | `GET /search.json` | [docs](https://serpapi.com/youtube-search-api) |
