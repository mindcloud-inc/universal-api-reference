# Datadog: Native API Reference

A consolidated summary of Datadog's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.datadoghq.com/api/latest/
- **API base URL:** `https://api.us5.datadoghq.com`

## Authentication

### API Key + Application Key

Connect with a Datadog API key and application key for the US5 site.

### Credentials

- **API Key:** `apiKey` · required
- **Application Key:** `applicationKey` · required · Datadog application key for read and management API calls.

Send these headers with each API request:

```http
DD-API-KEY: <apiKey>
DD-APPLICATION-KEY: <applicationKey>
```

[Official authentication documentation](https://docs.datadoghq.com/account_management/api-app-keys/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Downtime](actions/cancel-downtime.md) | `DELETE /api/v2/downtime/:downtime_id` | [docs](https://docs.datadoghq.com/api/latest/downtimes/#cancel-a-downtime) |
| [Create Dashboard](actions/create-dashboard.md) | `POST /api/v1/dashboard` | [docs](https://docs.datadoghq.com/api/latest/dashboards/#create-a-new-dashboard) |
| [Create Monitor](actions/create-monitor.md) | `POST /api/v1/monitor` | [docs](https://docs.datadoghq.com/api/latest/monitors/#create-a-monitor) |
| [Delete Dashboard](actions/delete-dashboard.md) | `DELETE /api/v1/dashboard/:dashboard_id` | [docs](https://docs.datadoghq.com/api/latest/dashboards/#delete-a-dashboard) |
| [Delete Monitor](actions/delete-monitor.md) | `DELETE /api/v1/monitor/:monitor_id` | [docs](https://docs.datadoghq.com/api/latest/monitors/#delete-a-monitor) |
| [Get Dashboard](actions/get-dashboard.md) | `GET /api/v1/dashboard/:dashboard_id` | [docs](https://docs.datadoghq.com/api/latest/dashboards/#get-a-dashboard) |
| [Get Downtime](actions/get-downtime.md) | `GET /api/v2/downtime/:downtime_id` | [docs](https://docs.datadoghq.com/api/latest/downtimes/#get-a-downtime) |
| [Get Monitor Details](actions/get-monitor-details.md) | `GET /api/v1/monitor/:monitor_id` | [docs](https://docs.datadoghq.com/api/latest/monitors/#get-a-monitors-details) |
| [Get Notebook](actions/get-notebook.md) | `GET /api/v1/notebooks/:notebook_id` | [docs](https://docs.datadoghq.com/api/latest/notebooks/#get-a-notebook) |
| [Get SLO History](actions/get-slo-history.md) | `GET /api/v1/slo/:slo_id/history` | [docs](https://docs.datadoghq.com/api/latest/service-level-objectives/#get-an-slos-history) |
| [List Active Metrics](actions/list-active-metrics.md) | `GET /api/v1/metrics` | [docs](https://docs.datadoghq.com/api/latest/metrics/#get-active-metrics-list) |
| [List Dashboards](actions/list-dashboards.md) | `GET /api/v1/dashboard` | [docs](https://docs.datadoghq.com/api/latest/dashboards/#get-all-dashboards) |
| [List Downtimes](actions/list-downtimes.md) | `GET /api/v2/downtime` | [docs](https://docs.datadoghq.com/api/latest/downtimes/#get-all-downtimes) |
| [List Events](actions/list-events.md) | `GET /api/v1/events` | [docs](https://docs.datadoghq.com/api/latest/events/#get-a-list-of-events) |
| [List Monitors](actions/list-monitors.md) | `GET /api/v1/monitor` | [docs](https://docs.datadoghq.com/api/latest/monitors/#get-all-monitors) |
| [List Notebooks](actions/list-notebooks.md) | `GET /api/v1/notebooks` | [docs](https://docs.datadoghq.com/api/latest/notebooks/#get-all-notebooks) |
| [List SLOs](actions/list-sl-os.md) | `GET /api/v1/slo` | [docs](https://docs.datadoghq.com/api/latest/service-level-objectives/#get-all-slos) |
| [Post Event](actions/post-event.md) | `POST /api/v1/events` | [docs](https://docs.datadoghq.com/api/latest/events/#post-an-event) |
| [Query Timeseries Points](actions/query-timeseries-points.md) | `GET /api/v1/query` | [docs](https://docs.datadoghq.com/api/latest/metrics/#query-timeseries-points) |
| [Schedule Downtime](actions/schedule-downtime.md) | `POST /api/v2/downtime` | [docs](https://docs.datadoghq.com/api/latest/downtimes/#schedule-a-downtime) |
| [Search Monitors](actions/search-monitors.md) | `GET /api/v1/monitor/search` | [docs](https://docs.datadoghq.com/api/latest/monitors/#monitors-search) |
| [Update Dashboard](actions/update-dashboard.md) | `PUT /api/v1/dashboard/:dashboard_id` | [docs](https://docs.datadoghq.com/api/latest/dashboards/#update-a-dashboard) |
| [Update Monitor](actions/update-monitor.md) | `PUT /api/v1/monitor/:monitor_id` | [docs](https://docs.datadoghq.com/api/latest/monitors/#edit-a-monitor) |
| [Validate Monitor](actions/validate-monitor.md) | `POST /api/v1/monitor/validate` | [docs](https://docs.datadoghq.com/api/latest/monitors/#validate-a-monitor) |
