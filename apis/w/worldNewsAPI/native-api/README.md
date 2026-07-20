# World News API: Native API Reference

A consolidated summary of World News API's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://worldnewsapi.com/docs/
- **API base URL:** `https://api.worldnewsapi.com`

## Authentication

### API Key

Send the tenant API key as the x-api-key request header for all World News API calls.

### Credentials

- **API Key:** `apiKey` · required · World News API tenant API key used as the x-api-key request header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://worldnewsapi.com/docs/authentication/)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract News](actions/extract-news.md) | `GET /extract-news` | [docs](https://worldnewsapi.com/docs/extract-news/) |
| [Extract News Links](actions/extract-news-links.md) | `GET /extract-news-links` | [docs](https://worldnewsapi.com/docs/extract-news-links/) |
| [Get Geo Coordinates](actions/get-geo-coordinates.md) | `GET /geo-coordinates` | [docs](https://worldnewsapi.com/docs/get-geo-coordinates/) |
| [Retrieve Front Page](actions/retrieve-front-page.md) | `GET /retrieve-front-page` | [docs](https://worldnewsapi.com/docs/newspaper-front-pages/) |
| [Retrieve News](actions/retrieve-news.md) | `GET /retrieve-news` | [docs](https://worldnewsapi.com/docs/retrieve-news/) |
| [Search News](actions/search-news.md) | `GET /search-news` | [docs](https://worldnewsapi.com/docs/search-news/) |
| [Search News Sources](actions/search-news-sources.md) | `GET /search-news-sources` | [docs](https://worldnewsapi.com/docs/search-news-sources/) |
| [Suggest News Source](actions/suggest-news-source.md) | `POST /suggest-news-source` | [docs](https://worldnewsapi.com/docs/suggest-news-source/) |
| [Top News](actions/top-news.md) | `GET /top-news` | [docs](https://worldnewsapi.com/docs/top-news/) |
| [Website to RSS Feed](actions/website-to-rss-feed.md) | `GET /feed.rss` | [docs](https://worldnewsapi.com/docs/website-to-rss-feed/) |
