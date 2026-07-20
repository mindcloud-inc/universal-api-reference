# <img src="https://images.mindcloud.co/apps/icons/bs_1777485988145.png" alt="Better Stack Telemetry logo" width="28" height="28"> Better Stack Telemetry: Universal API

Manage telemetry sources, source groups, metrics, dashboards, and connections.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/betterStackTelemetry/latest
- **Category:** IT Operations / Observability
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://betterstack.com/log-management
- **Vendor API docs:** https://betterstack.com/docs/logs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Dashboard](actions/export-dashboard.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/export-dashboard?connectionId=$CONNECTION_ID&id=164807" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Create Exploration Alert](actions/create-exploration-alert.md) | POST | Creates a new exploration alert in Better Stack Telemetry. |
| [List Alerts In Exploration](actions/list-alerts-in-exploration.md) | GET | Retrieves alerts in an exploration from Better Stack Telemetry. |
| [Remove Exploration Alert](actions/remove-exploration-alert.md) | DELETE | Deletes an existing exploration alert from Better Stack Telemetry. |
| [Update Exploration Alert](actions/update-exploration-alert.md) | PUT | Updates an existing exploration alert in Better Stack Telemetry. |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Export Dashboard](actions/export-dashboard.md) | GET | Exports a dashboard from Better Stack Telemetry. |
| [Get Dashboard](actions/get-dashboard.md) | GET | Retrieves a dashboard from Better Stack Telemetry. |
| [Import Dashboard](actions/import-dashboard.md) | POST | Imports a dashboard into Better Stack Telemetry. |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from Better Stack Telemetry. |
| [Remove Dashboard](actions/remove-dashboard.md) | DELETE | Deletes an existing dashboard from Better Stack Telemetry. |

### Dashboard Template

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboard Templates](actions/list-dashboard-templates.md) | GET | Retrieves dashboard templates from Better Stack Telemetry. |

### Exploration

| Action | Method | Description |
| --- | --- | --- |
| [Get Exploration](actions/get-exploration.md) | GET | Retrieves an exploration from Better Stack Telemetry. |
| [List Explorations](actions/list-explorations.md) | GET | Retrieves explorations from Better Stack Telemetry. |
| [Update Exploration](actions/update-exploration.md) | PUT | Updates an existing exploration in Better Stack Telemetry. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Create Metric](actions/create-metric.md) | POST | Creates a new metric in Better Stack Telemetry. |
| [List Metrics](actions/list-metrics.md) | GET | Retrieves metrics for a source from Better Stack Telemetry. |
| [Remove Metric](actions/remove-metric.md) | DELETE | Deletes an existing metric from Better Stack Telemetry. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a new telemetry source in Better Stack Telemetry. |
| [Get Source](actions/get-source.md) | GET | Retrieves a telemetry source from Better Stack Telemetry. |
| [List Sources](actions/list-sources.md) | GET | Retrieves telemetry sources from Better Stack Telemetry. |
| [List Sources In Source Group](actions/list-sources-in-source-group.md) | GET | Retrieves sources in a source group from Better Stack Telemetry. |
| [Remove Source](actions/remove-source.md) | DELETE | Deletes an existing telemetry source from Better Stack Telemetry. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing telemetry source in Better Stack Telemetry. |

### Source Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Source Group](actions/create-source-group.md) | POST | Creates a new source group in Better Stack Telemetry. |
| [Get Source Group](actions/get-source-group.md) | GET | Retrieves a source group from Better Stack Telemetry. |
| [List Source Groups](actions/list-source-groups.md) | GET | Retrieves source groups from Better Stack Telemetry. |
| [Remove Source Group](actions/remove-source-group.md) | DELETE | Deletes an existing source group from Better Stack Telemetry. |
| [Update Source Group](actions/update-source-group.md) | PUT | Updates an existing source group in Better Stack Telemetry. |

