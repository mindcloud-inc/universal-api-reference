# Better Stack Telemetry: Native API Reference

A consolidated summary of Better Stack Telemetry's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://betterstack.com/docs/logs/api/
- **API base URL:** `https://telemetry.betterstack.com`

## Authentication

### API Key

Use a Better Stack Telemetry API token in the Authorization header as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://betterstack.com/docs/logs/api/getting-started/)

## API conventions

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `pagination.next`.

## Pagination

Use `per_page` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Exploration Alert](actions/create-exploration-alert.md) | `POST /api/v2/explorations/:exploration_id/alerts` | [docs](https://betterstack.com/docs/logs/api/alerts/create/) |
| [Create Metric](actions/create-metric.md) | `POST /api/v2/sources/:source_id/metrics` | [docs](https://betterstack.com/docs/logs/api/creating-a-metric/) |
| [Create Source](actions/create-source.md) | `POST /api/v1/sources` | [docs](https://betterstack.com/docs/logs/api/create-a-source/) |
| [Create Source Group](actions/create-source-group.md) | `POST /api/v1/source-groups` | [docs](https://betterstack.com/docs/logs/api/create-a-source-group/) |
| [Export Dashboard](actions/export-dashboard.md) | `GET /api/v2/dashboards/:id/export` | [docs](https://betterstack.com/docs/logs/api/dashboards/export/) |
| [Get Dashboard](actions/get-dashboard.md) | `GET /api/v2/dashboards/:id` | [docs](https://betterstack.com/docs/logs/api/dashboards/get/) |
| [Get Exploration](actions/get-exploration.md) | `GET /api/v2/explorations/:id` | [docs](https://betterstack.com/docs/logs/api/explorations/get/) |
| [Get Source](actions/get-source.md) | `GET /api/v1/sources/:source_id` | [docs](https://betterstack.com/docs/logs/api/get-a-single-source/) |
| [Get Source Group](actions/get-source-group.md) | `GET /api/v1/source-groups/:source_group_id` | [docs](https://betterstack.com/docs/logs/api/getting-a-single-source-group/) |
| [Import Dashboard](actions/import-dashboard.md) | `POST /api/v2/dashboards/import` | [docs](https://betterstack.com/docs/logs/api/dashboards/import/) |
| [List Alerts In Exploration](actions/list-alerts-in-exploration.md) | `GET /api/v2/explorations/:exploration_id/alerts` | [docs](https://betterstack.com/docs/logs/api/alerts/list/) |
| [List Dashboard Templates](actions/list-dashboard-templates.md) | `GET /api/v2/dashboards/templates` | [docs](https://betterstack.com/docs/logs/api/dashboards/templates/) |
| [List Dashboards](actions/list-dashboards.md) | `GET /api/v2/dashboards` | [docs](https://betterstack.com/docs/logs/api/dashboards/list/) |
| [List Explorations](actions/list-explorations.md) | `GET /api/v2/explorations` | [docs](https://betterstack.com/docs/logs/api/explorations/list/) |
| [List Metrics](actions/list-metrics.md) | `GET /api/v2/sources/:source_id/metrics` | [docs](https://betterstack.com/docs/logs/api/list-all-existing-metrics/) |
| [List Source Groups](actions/list-source-groups.md) | `GET /api/v1/source-groups` | [docs](https://betterstack.com/docs/logs/api/list-all-existing-source-groups/) |
| [List Sources](actions/list-sources.md) | `GET /api/v1/sources` | [docs](https://betterstack.com/docs/logs/api/list-all-existing-sources/) |
| [List Sources In Source Group](actions/list-sources-in-source-group.md) | `GET /api/v1/source-groups/:id/sources` | [docs](https://betterstack.com/docs/logs/api/listing-sources-in-source-group/) |
| [Remove Dashboard](actions/remove-dashboard.md) | `DELETE /api/v2/dashboards/:id` | [docs](https://betterstack.com/docs/logs/api/dashboards/delete/) |
| [Remove Exploration Alert](actions/remove-exploration-alert.md) | `DELETE /api/v2/explorations/:exploration_id/alerts/:id` | [docs](https://betterstack.com/docs/logs/api/alerts/delete/) |
| [Remove Metric](actions/remove-metric.md) | `DELETE /api/v2/sources/:source_id/metrics/:id` | [docs](https://betterstack.com/docs/logs/api/deleting-an-existing-metric/) |
| [Remove Source](actions/remove-source.md) | `DELETE /api/v1/sources/:source_id` | [docs](https://betterstack.com/docs/logs/api/delete-an-existing-source/) |
| [Remove Source Group](actions/remove-source-group.md) | `DELETE /api/v1/source-groups/:source_group_id` | [docs](https://betterstack.com/docs/logs/api/deleting-an-existing-source-group/) |
| [Update Exploration](actions/update-exploration.md) | `PATCH /api/v2/explorations/:id` | [docs](https://betterstack.com/docs/logs/api/explorations/update/) |
| [Update Exploration Alert](actions/update-exploration-alert.md) | `PATCH /api/v2/explorations/:exploration_id/alerts/:id` | [docs](https://betterstack.com/docs/logs/api/alerts/update/) |
| [Update Source](actions/update-source.md) | `PATCH /api/v1/sources/:source_id` | [docs](https://betterstack.com/docs/logs/api/update-source/) |
| [Update Source Group](actions/update-source-group.md) | `PATCH /api/v1/source-groups/:source_group_id` | [docs](https://betterstack.com/docs/logs/api/updating-a-source-group/) |
