# Foreplay: Native API Reference

A consolidated summary of Foreplay's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.foreplay.co/
- **OpenAPI specification:** https://public.api.foreplay.co/openapi.json
- **API base URL:** `https://public.api.foreplay.co`

## Authentication

### API Key

Use a Foreplay API key generated from the Foreplay API dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.foreplay.co/en/articles/0374062-getting-started-with-the-foreplay-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Discover Brands by Ads](actions/discover-brands-by-ads.md) | `GET /api/discovery/brands/explore` | [docs](https://public.api.foreplay.co/openapi.json) |
| [Get Ad](actions/get-ad.md) | `GET /api/ad` | [docs](https://public.api.foreplay.co/openapi.json) |
| [Get Ad by ID](actions/get-ad-by-id.md) | `GET /api/ad/{ad_id}` | [docs](https://public.api.foreplay.co/openapi.json) |
| [Get Brand Analytics](actions/get-brand-analytics.md) | `GET /api/brand/analytics` | [docs](https://public.api.foreplay.co/openapi.json) |
| [Get Spyder Brand](actions/get-spyder-brand.md) | `GET /api/spyder/brand` | [docs](https://public.api.foreplay.co/openapi.json) |
| [Get Usage](actions/get-usage.md) | `GET /api/usage` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Ad Duplicates](actions/list-ad-duplicates.md) | `GET /api/ad/duplicates/{ad_id}` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Board Ads](actions/list-board-ads.md) | `GET /api/board/ads` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Board Brands](actions/list-board-brands.md) | `GET /api/board/brands` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Boards](actions/list-boards.md) | `GET /api/boards` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Brand Ads by Brand ID](actions/list-brand-ads-by-brand-id.md) | `GET /api/brand/getAdsByBrandId` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Brand Ads by Page ID](actions/list-brand-ads-by-page-id.md) | `GET /api/brand/getAdsByPageId` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Brands by Domain](actions/list-brands-by-domain.md) | `GET /api/brand/getBrandsByDomain` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Spyder Brand Ads](actions/list-spyder-brand-ads.md) | `GET /api/spyder/brand/ads` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Spyder Brands](actions/list-spyder-brands.md) | `GET /api/spyder/brands` | [docs](https://public.api.foreplay.co/openapi.json) |
| [List Swipefile Ads](actions/list-swipefile-ads.md) | `GET /api/swipefile/ads` | [docs](https://public.api.foreplay.co/openapi.json) |
| [Search Discovery Ads](actions/search-discovery-ads.md) | `GET /api/discovery/ads` | [docs](https://public.api.foreplay.co/openapi.json) |
| [Search Discovery Brands](actions/search-discovery-brands.md) | `GET /api/discovery/brands` | [docs](https://public.api.foreplay.co/openapi.json) |
