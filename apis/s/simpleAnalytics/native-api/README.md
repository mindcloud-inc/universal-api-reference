# Simple Analytics: Native API Reference

A consolidated summary of Simple Analytics's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.simpleanalytics.com/api/authenticate
- **API base URL:** `https://simpleanalytics.com`

## Authentication

### API Key + User ID

Use a Simple Analytics API key and user ID to access the Stats, Export, and Admin APIs.

### Credentials

- **API Key:** `apiKey` · required · Simple Analytics API key starting with `sa_api_key_...`. This is sent as the `Api-Key` header on every protected request.
- **User ID:** `userId` · required · Simple Analytics user ID starting with `sa_user_id_...`. This is sent as the `User-Id` header on every protected request.

Send these headers with each API request:

```http
Api-Key: <apiKey>
User-Id: <userId>
```

[Official authentication documentation](https://docs.simpleanalytics.com/api/authenticate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Website](actions/add-website.md) | `POST /api/websites/add` | [docs](https://docs.simpleanalytics.com/api/admin) |
| [Export Data Points](actions/export-data-points.md) | `GET /api/export/datapoints` | [docs](https://docs.simpleanalytics.com/api/export-data-points) |
| [Export Data Points CSV](actions/export-data-points-csv.md) | `GET /api/export/datapoints` | [docs](https://docs.simpleanalytics.com/api/export-data-points) |
| [Export Hourly Data CSV](actions/export-hourly-data-csv.md) | `GET /api/export/datapoints` | [docs](https://docs.simpleanalytics.com/api/export-data-points) |
| [Export Hourly Data JSON](actions/export-hourly-data-json.md) | `GET /api/export/datapoints` | [docs](https://docs.simpleanalytics.com/api/export-data-points) |
| [Get Browser Names Breakdown](actions/get-browser-names-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Countries Breakdown](actions/get-countries-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Device Types Breakdown](actions/get-device-types-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Event Counts](actions/get-event-counts.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Filtered Stats](actions/get-filtered-stats.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Histogram](actions/get-histogram.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get OS Names Breakdown](actions/get-os-names-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Page Stats](actions/get-page-stats.md) | `GET /{{hostname}}/{{pagePath}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Pages Breakdown](actions/get-pages-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Referrers Breakdown](actions/get-referrers-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Seconds On Page](actions/get-seconds-on-page.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get UTM Campaigns Breakdown](actions/get-utm-campaigns-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get UTM Contents Breakdown](actions/get-utm-contents-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get UTM Mediums Breakdown](actions/get-utm-mediums-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get UTM Sources Breakdown](actions/get-utm-sources-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get UTM Terms Breakdown](actions/get-utm-terms-breakdown.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [Get Website Stats](actions/get-website-stats.md) | `GET /{{hostname}}.json` | [docs](https://docs.simpleanalytics.com/api/stats) |
| [List Websites](actions/list-websites.md) | `GET /api/websites` | [docs](https://docs.simpleanalytics.com/api/admin) |
