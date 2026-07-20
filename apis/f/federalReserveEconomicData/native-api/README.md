# Federal Reserve Economic Data: Native API Reference

A consolidated summary of Federal Reserve Economic Data's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://fred.stlouisfed.org/docs/api/fred/overview.html
- **API base URL:** `https://api.stlouisfed.org`

## Authentication

### API Key

Authenticate FRED API requests with a registered FRED API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://fred.stlouisfed.org/docs/api/api_key.html)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | `GET /fred/category` | [docs](https://fred.stlouisfed.org/docs/api/fred/category.html) |
| [Get Release](actions/get-release.md) | `GET /fred/release` | [docs](https://fred.stlouisfed.org/docs/api/fred/release.html) |
| [Get Series](actions/get-series.md) | `GET /fred/series` | [docs](https://fred.stlouisfed.org/docs/api/fred/series.html) |
| [Get Series Release](actions/get-series-release.md) | `GET /fred/series/release` | [docs](https://fred.stlouisfed.org/docs/api/fred/series_release.html) |
| [Get Source](actions/get-source.md) | `GET /fred/source` | [docs](https://fred.stlouisfed.org/docs/api/fred/source.html) |
| [List Category Children](actions/list-category-children.md) | `GET /fred/category/children` | [docs](https://fred.stlouisfed.org/docs/api/fred/category_children.html) |
| [List Category Series](actions/list-category-series.md) | `GET /fred/category/series` | [docs](https://fred.stlouisfed.org/docs/api/fred/category_series.html) |
| [List Category Tags](actions/list-category-tags.md) | `GET /fred/category/tags` | [docs](https://fred.stlouisfed.org/docs/api/fred/category_tags.html) |
| [List Related Categories](actions/list-related-categories.md) | `GET /fred/category/related` | [docs](https://fred.stlouisfed.org/docs/api/fred/category_related.html) |
| [List Release Dates](actions/list-release-dates.md) | `GET /fred/releases/dates` | [docs](https://fred.stlouisfed.org/docs/api/fred/releases_dates.html) |
| [List Release Dates For Release](actions/list-release-dates-for-release.md) | `GET /fred/release/dates` | [docs](https://fred.stlouisfed.org/docs/api/fred/release_dates.html) |
| [List Release Series](actions/list-release-series.md) | `GET /fred/release/series` | [docs](https://fred.stlouisfed.org/docs/api/fred/release_series.html) |
| [List Release Sources](actions/list-release-sources.md) | `GET /fred/release/sources` | [docs](https://fred.stlouisfed.org/docs/api/fred/release_sources.html) |
| [List Releases](actions/list-releases.md) | `GET /fred/releases` | [docs](https://fred.stlouisfed.org/docs/api/fred/releases.html) |
| [List Series Categories](actions/list-series-categories.md) | `GET /fred/series/categories` | [docs](https://fred.stlouisfed.org/docs/api/fred/series_categories.html) |
| [List Series Observations](actions/list-series-observations.md) | `GET /fred/series/observations` | [docs](https://fred.stlouisfed.org/docs/api/fred/series_observations.html) |
| [List Series Updates](actions/list-series-updates.md) | `GET /fred/series/updates` | [docs](https://fred.stlouisfed.org/docs/api/fred/series_updates.html) |
| [List Source Releases](actions/list-source-releases.md) | `GET /fred/source/releases` | [docs](https://fred.stlouisfed.org/docs/api/fred/source_releases.html) |
| [List Sources](actions/list-sources.md) | `GET /fred/sources` | [docs](https://fred.stlouisfed.org/docs/api/fred/sources.html) |
| [Search Series](actions/search-series.md) | `GET /fred/series/search` | [docs](https://fred.stlouisfed.org/docs/api/fred/series_search.html) |
