# Umami: Native API Reference

A consolidated summary of Umami's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.umami.is/docs/api
- **API base URL:** `https://api.umami.is/v1`

## Authentication

### API Key

Connect to Umami Cloud with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.umami.is/docs/cloud/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `pageSize` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Website](actions/create-website.md) | `POST /websites` | [docs](https://docs.umami.is/docs/api/websites) |
| [Get Active Visitors](actions/get-active-visitors.md) | `GET /websites/:websiteId/active` | [docs](https://docs.umami.is/docs/api/website-stats) |
| [Get Event Data](actions/get-event-data.md) | `GET /websites/:websiteId/event-data/:eventId` | [docs](https://docs.umami.is/docs/api/events) |
| [Get Event Data Events](actions/get-event-data-events.md) | `GET /websites/:websiteId/event-data/events` | [docs](https://docs.umami.is/docs/api/events) |
| [Get Event Series](actions/get-event-series.md) | `GET /websites/:websiteId/events/series` | [docs](https://docs.umami.is/docs/api/website-stats) |
| [Get Event Stats](actions/get-event-stats.md) | `GET /websites/:websiteId/events/stats` | [docs](https://docs.umami.is/docs/api/events) |
| [Get Expanded Website Metrics](actions/get-expanded-website-metrics.md) | `GET /websites/:websiteId/metrics/expanded` | [docs](https://docs.umami.is/docs/api/website-stats) |
| [Get Realtime](actions/get-realtime.md) | `GET /realtime/:websiteId` | [docs](https://docs.umami.is/docs/api/realtime) |
| [Get Session](actions/get-session.md) | `GET /websites/:websiteId/sessions/:sessionId` | [docs](https://docs.umami.is/docs/api/sessions) |
| [Get Session Activity](actions/get-session-activity.md) | `GET /websites/:websiteId/sessions/:sessionId/activity` | [docs](https://docs.umami.is/docs/api/sessions) |
| [Get Session Stats](actions/get-session-stats.md) | `GET /websites/:websiteId/sessions/stats` | [docs](https://docs.umami.is/docs/api/sessions) |
| [Get Website](actions/get-website.md) | `GET /websites/:websiteId` | [docs](https://docs.umami.is/docs/api/websites) |
| [Get Website Date Range](actions/get-website-date-range.md) | `GET /websites/:websiteId/daterange` | [docs](https://docs.umami.is/docs/api/website-stats) |
| [Get Website Metrics](actions/get-website-metrics.md) | `GET /websites/:websiteId/metrics` | [docs](https://docs.umami.is/docs/api/website-stats) |
| [Get Website Pageviews](actions/get-website-pageviews.md) | `GET /websites/:websiteId/pageviews` | [docs](https://docs.umami.is/docs/api/website-stats) |
| [Get Website Stats](actions/get-website-stats.md) | `GET /websites/:websiteId/stats` | [docs](https://docs.umami.is/docs/api/website-stats) |
| [Get Weekly Sessions](actions/get-weekly-sessions.md) | `GET /websites/:websiteId/sessions/weekly` | [docs](https://docs.umami.is/docs/api/sessions) |
| [List Event Data](actions/list-event-data.md) | `GET /websites/:websiteId/event-data` | [docs](https://docs.umami.is/docs/api/events) |
| [List Events](actions/list-events.md) | `GET /websites/:websiteId/events` | [docs](https://docs.umami.is/docs/api/events) |
| [List Session Properties](actions/list-session-properties.md) | `GET /websites/:websiteId/session-data/properties` | [docs](https://docs.umami.is/docs/api/sessions) |
| [List Session Property Values](actions/list-session-property-values.md) | `GET /websites/:websiteId/session-data/values` | [docs](https://docs.umami.is/docs/api/sessions) |
| [List Sessions](actions/list-sessions.md) | `GET /websites/:websiteId/sessions` | [docs](https://docs.umami.is/docs/api/sessions) |
| [List Websites](actions/list-websites.md) | `GET /websites` | [docs](https://docs.umami.is/docs/api/websites) |
| [Update Website](actions/update-website.md) | `POST /websites/:websiteId` | [docs](https://docs.umami.is/docs/api/websites) |
