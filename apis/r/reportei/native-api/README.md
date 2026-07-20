# Reportei: Native API Reference

A consolidated summary of Reportei's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developers.reportei.com
- **API base URL:** `https://app.reportei.com/api/v2`

## Authentication

### Bearer Token

Authenticate requests with a Reportei API bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.reportei.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `descending`. Use `false` for ascending order and `true` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Dashboard](actions/create-dashboard.md) | `POST /dashboards` | [docs](https://developers.reportei.com#dashboards-endpoint-2) |
| [Create Report](actions/create-report.md) | `POST /reports` | [docs](https://developers.reportei.com#relatorios-endpoint-2) |
| [Create Timeline Event](actions/create-timeline-event.md) | `POST /timeline-events` | [docs](https://developers.reportei.com#timeline-endpoint-2) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.reportei.com#webhooks-endpoint-3) |
| [Delete Timeline Event](actions/delete-timeline-event.md) | `DELETE /timeline-events/:id` | [docs](https://developers.reportei.com#timeline-endpoint-4) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://developers.reportei.com#webhooks-endpoint-5) |
| [Get Company Settings](actions/get-company-settings.md) | `GET /companies/settings` | [docs](https://developers.reportei.com#empresas-endpoint-0) |
| [Get Dashboard](actions/get-dashboard.md) | `GET /dashboards/:id` | [docs](https://developers.reportei.com#dashboards-endpoint-1) |
| [Get Integration](actions/get-integration.md) | `GET /integrations/:id` | [docs](https://developers.reportei.com#integracoes-endpoint-1) |
| [Get Metric Data](actions/get-metric-data.md) | `POST /metrics/get-data` | [docs](https://developers.reportei.com#metricas-endpoint-1) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://developers.reportei.com#projetos-endpoint-1) |
| [Get Report](actions/get-report.md) | `GET /reports/:id` | [docs](https://developers.reportei.com#relatorios-endpoint-1) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://developers.reportei.com#templates-endpoint-1) |
| [Get Timeline Event](actions/get-timeline-event.md) | `GET /timeline-events/:id` | [docs](https://developers.reportei.com#timeline-endpoint-1) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://developers.reportei.com#webhooks-endpoint-2) |
| [List Dashboards](actions/list-dashboards.md) | `GET /dashboards` | [docs](https://developers.reportei.com#dashboards-endpoint-0) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://developers.reportei.com#integracoes-endpoint-0) |
| [List Metrics](actions/list-metrics.md) | `GET /metrics` | [docs](https://developers.reportei.com#metricas-endpoint-0) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.reportei.com#projetos-endpoint-0) |
| [List Reports](actions/list-reports.md) | `GET /reports` | [docs](https://developers.reportei.com#relatorios-endpoint-0) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.reportei.com#templates-endpoint-0) |
| [List Timeline Events](actions/list-timeline-events.md) | `GET /timeline-events` | [docs](https://developers.reportei.com#timeline-endpoint-0) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /webhooks/events` | [docs](https://developers.reportei.com#webhooks-endpoint-1) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.reportei.com#webhooks-endpoint-0) |
| [Update Timeline Event](actions/update-timeline-event.md) | `PUT /timeline-events/:id` | [docs](https://developers.reportei.com#timeline-endpoint-3) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:id` | [docs](https://developers.reportei.com#webhooks-endpoint-4) |
