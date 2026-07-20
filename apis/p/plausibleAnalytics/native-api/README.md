# Plausible Analytics: Native API Reference

A consolidated summary of Plausible Analytics's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://plausible.io/docs
- **API base URL:** `https://plausible.io`

## Authentication

### API Key

Use a Plausible API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://plausible.io/docs/stats-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `meta.after`.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Behavioral Filters](actions/apply-behavioral-filters.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Check API Health](actions/check-api-health.md) | `GET /api/health` | [docs](https://plausible.io/docs/events-api) |
| [Create Custom Property](actions/create-custom-property.md) | `PUT /api/v1/sites/custom-props` | [docs](https://plausible.io/docs/sites-api) |
| [Create Site](actions/create-site.md) | `POST /api/v1/sites` | [docs](https://plausible.io/docs/sites-api) |
| [Delete Custom Property](actions/delete-custom-property.md) | `DELETE /api/v1/sites/custom-props/:property` | [docs](https://plausible.io/docs/sites-api) |
| [Delete Goal](actions/delete-goal.md) | `DELETE /api/v1/sites/goals/:goalId` | [docs](https://plausible.io/docs/sites-api) |
| [Delete Guest](actions/delete-guest.md) | `DELETE /api/v1/sites/guests/:email` | [docs](https://plausible.io/docs/sites-api) |
| [Delete Site](actions/delete-site.md) | `DELETE /api/v1/sites/:domain` | [docs](https://plausible.io/docs/sites-api) |
| [Filter by Page and Country](actions/filter-by-page-and-country.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Filter by Segment](actions/filter-by-segment.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Filter Case Insensitively](actions/filter-case-insensitively.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Browser Breakdown](actions/get-browser-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Campaign Breakdown](actions/get-campaign-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Channel Breakdown](actions/get-channel-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get City Breakdown](actions/get-city-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Country and City Analysis](actions/get-country-and-city-analysis.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Custom Date Range Stats](actions/get-custom-date-range-stats.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Custom Property Breakdown](actions/get-custom-property-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Device Breakdown](actions/get-device-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Entry Pages](actions/get-entry-pages.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Exit Pages](actions/get-exit-pages.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Goal Conversions](actions/get-goal-conversions.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Hourly Time Labels](actions/get-hourly-time-labels.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Landing Pages](actions/get-landing-pages.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Operating System Breakdown](actions/get-operating-system-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Realtime Visitors](actions/get-realtime-visitors.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Referrer Breakdown](actions/get-referrer-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Region Breakdown](actions/get-region-breakdown.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Revenue Metrics](actions/get-revenue-metrics.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Site](actions/get-site.md) | `GET /api/v1/sites/:domain` | [docs](https://plausible.io/docs/sites-api) |
| [Get Time Series](actions/get-time-series.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Top Countries](actions/get-top-countries.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Top Pages](actions/get-top-pages.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Top Sources](actions/get-top-sources.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get Traffic Summary](actions/get-traffic-summary.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Get UTM Source Analysis](actions/get-utm-source-analysis.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Include Imported Data](actions/include-imported-data.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Invite Guest](actions/invite-guest.md) | `PUT /api/v1/sites/guests` | [docs](https://plausible.io/docs/sites-api) |
| [List Custom Properties](actions/list-custom-properties.md) | `GET /api/v1/sites/custom-props` | [docs](https://plausible.io/docs/sites-api) |
| [List Goals](actions/list-goals.md) | `GET /api/v1/sites/goals` | [docs](https://plausible.io/docs/sites-api) |
| [List Guests](actions/list-guests.md) | `GET /api/v1/sites/guests` | [docs](https://plausible.io/docs/sites-api) |
| [List Sites](actions/list-sites.md) | `GET /api/v1/sites` | [docs](https://plausible.io/docs/sites-api) |
| [List Teams](actions/list-teams.md) | `GET /api/v1/sites/teams` | [docs](https://plausible.io/docs/sites-api) |
| [Paginate Stats Results](actions/paginate-stats-results.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Query by Custom Properties](actions/query-by-custom-properties.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Query Stats](actions/query-stats.md) | `POST /api/v2/query` | [docs](https://plausible.io/docs/stats-api) |
| [Send Event](actions/send-event.md) | `POST /api/event` | [docs](https://plausible.io/docs/events-api) |
| [Update Site](actions/update-site.md) | `PUT /api/v1/sites/:domain` | [docs](https://plausible.io/docs/sites-api) |
| [Upsert Goal](actions/upsert-goal.md) | `PUT /api/v1/sites/goals` | [docs](https://plausible.io/docs/sites-api) |
| [Upsert Shared Link](actions/upsert-shared-link.md) | `PUT /api/v1/sites/shared-links` | [docs](https://plausible.io/docs/sites-api) |
