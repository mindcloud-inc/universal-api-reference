# Agility CMS: Native API Reference

A consolidated summary of Agility CMS's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://agilitycms.com/docs/developers/content-fetch-api
- **OpenAPI specification:** https://api.aglty.io/swagger/v1/swagger.json
- **API base URL:** `https://api.aglty.io`

## Authentication

### API Key Header

Use an Agility CMS preview or fetch API key in the APIKey header.

### Credentials

- **API Key:** `apiKey` · required · The Agility CMS API key sent in the exact request header APIKey.

Send these headers with each API request:

```http
APIKey: <apiKey>
```

[Official authentication documentation](https://agilitycms.com/docs/developers/content-fetch-api)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The Agility CMS instance GUID, for example d076b104-u. |
| `locale` | path | `string` | yes | The locale code to retrieve content for, for example en-us. |

## Pagination

Use `Take` in the query string to set the page size (default 10; accepted range 1–250). Use `Skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `Sort` in the query string. Set the direction separately with `Direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Content Item (Fetch)](actions/get-content-item-fetch.md) | `GET /:guid/fetch/:locale/item/:id` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Content Item (Preview)](actions/get-content-item-preview.md) | `GET /:guid/preview/:locale/item/:id` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Content Item V1 (Fetch)](actions/get-content-item-v1-fetch.md) | `GET /v1/:guid/fetch/:locale/item/:id` | [docs](https://api.aglty.io/swagger/v1/swagger.json) |
| [Get Content Item V1 (Preview)](actions/get-content-item-v1-preview.md) | `GET /v1/:guid/preview/:locale/item/:id` | [docs](https://api.aglty.io/swagger/v1/swagger.json) |
| [Get Content Models (Fetch)](actions/get-content-models-fetch.md) | `GET /:guid/fetch/contentmodels` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Content Models (Preview)](actions/get-content-models-preview.md) | `GET /:guid/preview/contentmodels` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Gallery (Fetch)](actions/get-gallery-fetch.md) | `GET /v2/:guid/fetch/gallery/:id` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Gallery (Preview)](actions/get-gallery-preview.md) | `GET /v2/:guid/preview/gallery/:id` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Page By ID (Fetch)](actions/get-page-by-id-fetch.md) | `GET /:guid/fetch/:locale/page/:id` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Page By ID (Preview)](actions/get-page-by-id-preview.md) | `GET /:guid/preview/:locale/page/:id` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Page By ID V1 (Fetch)](actions/get-page-by-id-v1-fetch.md) | `GET /v1/:guid/fetch/:locale/page/:id` | [docs](https://api.aglty.io/swagger/v1/swagger.json) |
| [Get Page By ID V1 (Preview)](actions/get-page-by-id-v1-preview.md) | `GET /v1/:guid/preview/:locale/page/:id` | [docs](https://api.aglty.io/swagger/v1/swagger.json) |
| [Get Page By Path (Fetch)](actions/get-page-by-path-fetch.md) | `GET /:guid/fetch/:locale/page/:channel` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Page By Path (Preview)](actions/get-page-by-path-preview.md) | `GET /:guid/preview/:locale/page/:channel` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Sitemap Flat (Fetch)](actions/get-sitemap-flat-fetch.md) | `GET /:guid/fetch/:locale/sitemap/flat/:channelName` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Sitemap Flat (Preview)](actions/get-sitemap-flat-preview.md) | `GET /:guid/preview/:locale/sitemap/flat/:channelName` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Sitemap Nested (Fetch)](actions/get-sitemap-nested-fetch.md) | `GET /:guid/fetch/:locale/sitemap/nested/:channelName` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get Sitemap Nested (Preview)](actions/get-sitemap-nested-preview.md) | `GET /:guid/preview/:locale/sitemap/nested/:channelName` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get URL Redirections (Fetch)](actions/get-url-redirections-fetch.md) | `GET /:guid/fetch/urlredirection` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Get URL Redirections (Preview)](actions/get-url-redirections-preview.md) | `GET /:guid/preview/urlredirection` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [List Categories (Fetch)](actions/list-categories-fetch.md) | `GET /:guid/fetch/:locale/list/categories` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [List Categories (Preview)](actions/list-categories-preview.md) | `GET /:guid/preview/:locale/list/categories` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [List Content Items (Fetch)](actions/list-content-items-fetch.md) | `GET /:guid/fetch/:locale/list/:referenceName` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [List Content Items (Preview)](actions/list-content-items-preview.md) | `GET /:guid/preview/:locale/list/:referenceName` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [List Content Items V1 (Fetch)](actions/list-content-items-v1-fetch.md) | `GET /v1/:guid/fetch/:locale/list/:referenceName` | [docs](https://api.aglty.io/swagger/v1/swagger.json) |
| [List Content Items V1 (Preview)](actions/list-content-items-v1-preview.md) | `GET /v1/:guid/preview/:locale/list/:referenceName` | [docs](https://api.aglty.io/swagger/v1/swagger.json) |
| [List Posts (Fetch)](actions/list-posts-fetch.md) | `GET /:guid/fetch/:locale/list/posts` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [List Posts (Preview)](actions/list-posts-preview.md) | `GET /:guid/preview/:locale/list/posts` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Sync Content Items (Fetch)](actions/sync-content-items-fetch.md) | `GET /:guid/fetch/:locale/sync/items` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Sync Content Items (Preview)](actions/sync-content-items-preview.md) | `GET /:guid/preview/:locale/sync/items` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Sync Pages (Fetch)](actions/sync-pages-fetch.md) | `GET /:guid/fetch/:locale/sync/pages` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
| [Sync Pages (Preview)](actions/sync-pages-preview.md) | `GET /:guid/preview/:locale/sync/pages` | [docs](https://api.aglty.io/swagger/v2/swagger.json) |
