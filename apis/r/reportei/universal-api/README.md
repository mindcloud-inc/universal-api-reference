# <img src="https://images.mindcloud.co/apps/icons/reportei_1774885696716.png" alt="Reportei logo" width="28" height="28"> Reportei: Universal API

Create marketing reports and dashboards, manage projects, integrations, webhooks, and metrics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reportei/latest
- **Category:** Marketing
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reportei.com
- **Vendor API docs:** https://developers.reportei.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Settings](actions/get-company-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Company Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET | Retrieves company settings from Reportei. |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Create Dashboard](actions/create-dashboard.md) | POST | Creates a new dashboard in Reportei. |
| [Get Dashboard](actions/get-dashboard.md) | GET | Retrieves a dashboard from Reportei. |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from Reportei. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from Reportei. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from Reportei. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [List Metrics](actions/list-metrics.md) | GET | Retrieves metrics from Reportei. |

### Metric Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Metric Data](actions/get-metric-data.md) | GET | Retrieves metric data from Reportei. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Reportei. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Reportei. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Create Report](actions/create-report.md) | POST | Creates a new report in Reportei. |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from Reportei. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from Reportei. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Reportei. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Reportei. |

### Timeline Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Timeline Event](actions/create-timeline-event.md) | POST | Creates a new timeline event in Reportei. |
| [Delete Timeline Event](actions/delete-timeline-event.md) | DELETE | Deletes an existing timeline event from Reportei. |
| [Get Timeline Event](actions/get-timeline-event.md) | GET | Retrieves a timeline event from Reportei. |
| [List Timeline Events](actions/list-timeline-events.md) | GET | Retrieves timeline events from Reportei. |
| [Update Timeline Event](actions/update-timeline-event.md) | PUT | Updates an existing timeline event in Reportei. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Reportei. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Reportei. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Reportei. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Reportei. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Reportei. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET | Retrieves webhook event types from Reportei. |

