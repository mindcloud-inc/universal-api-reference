# Motive: Native API Reference

A consolidated summary of Motive's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developer.gomotive.com/reference/getting-started-with-your-api
- **API base URL:** `https://api.gomotive.com`

## Authentication

### API Key

Authenticate Motive API requests with the company X-API-KEY header.

### Credentials

- **X-API-KEY:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developer-docs.gomotive.com/docs/introduction)

## Pagination

Use `per_page` in the query string to set the page size. Use `page_no` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List assets](actions/list-assets.md) | `GET /v1/assets` | [docs](https://developer-docs.gomotive.com/reference/list-all-the-company-assets) |
| [List driver performance events](actions/list-driver-performance-events.md) | `GET /v1/driver_performance_events` | [docs](https://developer-docs.gomotive.com/reference/fetch-all-the-drivers-performance-events) |
| [List driver utilization](actions/list-driver-utilization.md) | `GET /v2/driver_utilization` | [docs](https://developer-docs.gomotive.com/reference/fetch-the-utilization-of-the-driver-v2) |
| [List scorecard summaries](actions/list-scorecard-summaries.md) | `GET /v1/scorecard_summary` | [docs](https://developer-docs.gomotive.com/reference/fetch-a-list-of-the-scorecard-summaries-of-the-companys-vehicles) |
| [List users](actions/list-users.md) | `GET /v1/users` | [docs](https://developer-docs.gomotive.com/reference/list-all-the-users-of-a-company) |
| [List vehicle utilization](actions/list-vehicle-utilization.md) | `GET /v1/vehicle_utilization` | [docs](https://developer-docs.gomotive.com/reference/fetch-the-utilization-of-the-driver-v2-1) |
| [List vehicles](actions/list-vehicles.md) | `GET /v1/vehicles` | [docs](https://developer-docs.gomotive.com/reference/list-all-the-company-vehicles) |
