# Chicago Transit Authority: Native API Reference

A consolidated summary of Chicago Transit Authority's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.transitchicago.com/developers/default.aspx
- **API base URL:** `https://lapi.transitchicago.com/api/1.0`

## Authentication

### CTA API Key

API key for CTA Train Tracker actions. Train actions pass the key as an endpoint-scoped hidden query argument; route status and alerts remain authless.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.transitchicago.com/developers/ttdocs/default.aspx)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Route Status by Route IDs](actions/get-route-status-by-route-ids.md) | `GET /routes.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [Get Station Status by Station IDs](actions/get-station-status-by-station-ids.md) | `GET /routes.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [Get Train Arrivals by Platform Stop](actions/get-train-arrivals-by-platform-stop.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [Get Train Arrivals by Platform Stop and Route](actions/get-train-arrivals-by-platform-stop-and-route.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [Get Train Arrivals by Platform Stop Limit](actions/get-train-arrivals-by-platform-stop-limit.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [Get Train Arrivals by Platform Stop Route Limit](actions/get-train-arrivals-by-platform-stop-route-limit.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [Get Train Arrivals by Station](actions/get-train-arrivals-by-station.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [Get Train Arrivals by Station and Route](actions/get-train-arrivals-by-station-and-route.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [Get Train Arrivals by Station Limit](actions/get-train-arrivals-by-station-limit.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [Get Train Arrivals by Station Route Limit](actions/get-train-arrivals-by-station-route-limit.md) | `GET /ttarrivals.aspx` | [docs](https://www.transitchicago.com/developers/ttdocs/default.aspx) |
| [List Active Alerts](actions/list-active-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Active Route Alerts](actions/list-active-route-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Active Station Alerts](actions/list-active-station-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Active Unplanned Alerts](actions/list-active-unplanned-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Alerts by Route IDs](actions/list-alerts-by-route-ids.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Alerts by Start Date](actions/list-alerts-by-start-date.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Alerts by Station IDs](actions/list-alerts-by-station-ids.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Bus Route Statuses](actions/list-bus-route-statuses.md) | `GET /routes.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Detailed Alerts](actions/list-detailed-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Non-Accessibility Alerts](actions/list-non-accessibility-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Planned Route Alerts](actions/list-planned-route-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Planned Station Alerts](actions/list-planned-station-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Rail Route Statuses](actions/list-rail-route-statuses.md) | `GET /routes.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Recent Alerts](actions/list-recent-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Recent Route Alerts](actions/list-recent-route-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Recent Station Alerts](actions/list-recent-station-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Route Statuses](actions/list-route-statuses.md) | `GET /routes.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Station Statuses](actions/list-station-statuses.md) | `GET /routes.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Systemwide Statuses](actions/list-systemwide-statuses.md) | `GET /routes.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
| [List Unplanned Alerts](actions/list-unplanned-alerts.md) | `GET /alerts.aspx` | [docs](https://www.transitchicago.com/assets/1/6/cta_Customer_Alerts_API_Developer_Guide_and_Documentation_20160929.pdf) |
