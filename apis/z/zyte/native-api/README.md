# Zyte: Native API Reference

A consolidated summary of Zyte's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.zyte.com/zyte-api/usage/stats.html
- **API base URL:** `https://zyte-api-stats.zyte.com`

## Authentication

### Dashboard API Key (Basic Auth)

Authenticate to Zyte Stats with your dashboard API key as the Basic-auth username and an empty password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Organization ID:** `organizationId` · required · Your Zyte organization ID, available in the Zyte dashboard and required by the Stats API.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.zyte.com/zyte-api/usage/stats.html)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_time` | query | `string` | no | Optional end of the reporting window in ISO 8601 format. Defaults to the current time when omitted by Zyte. |
| `start_time` | query | `string` | no | Optional start of the reporting window in ISO 8601 format. Defaults to seven days ago when omitted by Zyte. |

## Pagination

Use `page_size` in the query string to set the page size (default 25; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Actions Feature Usage](actions/get-actions-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Article Extraction Usage](actions/get-article-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Article List Extraction Usage](actions/get-article-list-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Article Navigation Extraction Usage](actions/get-article-navigation-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Browser HTML Extraction Source Usage](actions/get-browser-html-extraction-source-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Browser HTML Feature Usage](actions/get-browser-html-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Daily Domain Usage Trend](actions/get-daily-domain-usage-trend.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Daily Usage Trend](actions/get-daily-usage-trend.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Domain Health Breakdown](actions/get-domain-health-breakdown.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Domain Usage Breakdown](actions/get-domain-usage-breakdown.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Extended Geolocation Feature Usage](actions/get-extended-geolocation-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get File Download Feature Usage](actions/get-file-download-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Forum Thread Extraction Usage](actions/get-forum-thread-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Hourly Usage Trend](actions/get-hourly-usage-trend.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get HTTP Response Body Extraction Source Usage](actions/get-http-response-body-extraction-source-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get HTTP Response Body Feature Usage](actions/get-http-response-body-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Job Posting Extraction Usage](actions/get-job-posting-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Job Posting Navigation Extraction Usage](actions/get-job-posting-navigation-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Monthly Usage Trend](actions/get-monthly-usage-trend.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Network Capture Feature Usage](actions/get-network-capture-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Not Found Response Usage](actions/get-not-found-response-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Product Extraction Usage](actions/get-product-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Product List Extraction Usage](actions/get-product-list-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Product Navigation Extraction Usage](actions/get-product-navigation-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Screenshot Feature Usage](actions/get-screenshot-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get SERP Extraction Usage](actions/get-serp-extraction-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Session Context Feature Usage](actions/get-session-context-feature-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Successful Response Usage](actions/get-successful-response-usage.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Usage Overview](actions/get-usage-overview.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Yearly Domain Usage Trend](actions/get-yearly-domain-usage-trend.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
| [Get Yearly Usage Trend](actions/get-yearly-usage-trend.md) | `GET /api/stats` | [docs](https://docs.zyte.com/zyte-api/usage/stats.html) |
