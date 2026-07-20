# <img src="https://images.mindcloud.co/apps/icons/datadog_1773857735984.png" alt="Datadog logo" width="28" height="28"> Datadog: Universal API

Observability API wrapper for Datadog monitors, dashboards, downtimes, metrics, events, SLOs, and notebooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datadog/latest
- **Category:** IT Operations / Observability
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datadoghq.com
- **Vendor API docs:** https://docs.datadoghq.com/api/latest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Monitors](actions/list-monitors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Create Dashboard](actions/create-dashboard.md) | POST | Creates a new dashboard in Datadog. |
| [Delete Dashboard](actions/delete-dashboard.md) | DELETE | Deletes an existing dashboard from Datadog. |
| [Get Dashboard](actions/get-dashboard.md) | GET | Retrieves a dashboard from Datadog. |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from Datadog. |
| [Update Dashboard](actions/update-dashboard.md) | PUT | Updates an existing dashboard in Datadog. |

### Downtime

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Downtime](actions/cancel-downtime.md) | DELETE | Cancels an existing downtime in Datadog. |
| [Get Downtime](actions/get-downtime.md) | GET | Retrieves a downtime from Datadog. |
| [List Downtimes](actions/list-downtimes.md) | GET | Retrieves downtimes from Datadog. |
| [Schedule Downtime](actions/schedule-downtime.md) | POST | Creates a new downtime in Datadog. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from Datadog. |
| [Post Event](actions/post-event.md) | POST | Creates a new event in Datadog. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [List Active Metrics](actions/list-active-metrics.md) | GET | Retrieves active metrics from Datadog. |
| [Query Timeseries Points](actions/query-timeseries-points.md) | GET | Retrieves timeseries points from Datadog. |

### Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Create Monitor](actions/create-monitor.md) | POST | Creates a new monitor in Datadog. |
| [Delete Monitor](actions/delete-monitor.md) | DELETE | Deletes an existing monitor from Datadog. |
| [Get Monitor Details](actions/get-monitor-details.md) | GET | Retrieves monitor details from Datadog. |
| [List Monitors](actions/list-monitors.md) | GET | Retrieves monitors from Datadog. |
| [Search Monitors](actions/search-monitors.md) | GET | Finds monitors in Datadog by query. |
| [Update Monitor](actions/update-monitor.md) | PUT | Updates an existing monitor in Datadog. |
| [Validate Monitor](actions/validate-monitor.md) | GET | Validates a monitor configuration in Datadog. |

### Notebook

| Action | Method | Description |
| --- | --- | --- |
| [Get Notebook](actions/get-notebook.md) | GET | Retrieves a notebook from Datadog. |
| [List Notebooks](actions/list-notebooks.md) | GET | Retrieves notebooks from Datadog. |

### Service Level Objective

| Action | Method | Description |
| --- | --- | --- |
| [Get SLO History](actions/get-slo-history.md) | GET | Retrieves service level objective history from Datadog. |
| [List SLOs](actions/list-sl-os.md) | GET | Retrieves service level objectives from Datadog. |

