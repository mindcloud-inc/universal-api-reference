# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-05-08-as-12_1778255631391.png" alt="Coralogix logo" width="28" height="28"> Coralogix: Universal API

Observability API wrapper for Coralogix alerts, dashboards, incidents, data usage, integrations, notifications, parsing rules, SLOs, and platform configuration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coralogix/latest
- **Category:** IT Operations / Observability
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coralogix.com
- **Vendor API docs:** https://docs.coralogix.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List System Roles](actions/list-system-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-system-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Filter Option Counts](actions/get-alert-filter-option-counts.md) | GET |  |
| [List Alert Definitions](actions/list-alert-definitions.md) | GET |  |
| [List Alert Scheduler Rules](actions/list-alert-scheduler-rules.md) | GET |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [List Send Data API Keys](actions/list-send-data-api-keys.md) | GET |  |

### Archive

| Action | Method | Description |
| --- | --- | --- |
| [Get Logs Archive Target](actions/get-logs-archive-target.md) | GET |  |

### Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get System Default Case Team Config](actions/get-system-default-case-team-config.md) | GET |  |

### Connector

| Action | Method | Description |
| --- | --- | --- |
| [Get Connector Type Summaries](actions/get-connector-type-summaries.md) | GET |  |
| [List Connector Summaries](actions/list-connector-summaries.md) | GET |  |
| [List Notification Connectors](actions/list-notification-connectors.md) | GET |  |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard Catalog](actions/get-dashboard-catalog.md) | GET |  |

### Enrichment

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Enrichment Settings](actions/get-company-enrichment-settings.md) | GET |  |
| [Get Enrichment Limit](actions/get-enrichment-limit.md) | GET |  |
| [List Custom Enrichments](actions/list-custom-enrichments.md) | GET |  |
| [List Enrichments](actions/list-enrichments.md) | GET |  |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [List Notification Entity Types](actions/list-notification-entity-types.md) | GET |  |

### Extension

| Action | Method | Description |
| --- | --- | --- |
| [List Deployed Extensions](actions/list-deployed-extensions.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboard Folders](actions/list-dashboard-folders.md) | GET |  |
| [List View Folders](actions/list-view-folders.md) | GET |  |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [List Incident Aggregations](actions/list-incident-aggregations.md) | GET |  |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Contextual Data Integrations](actions/list-contextual-data-integrations.md) | GET |  |
| [List Integrations](actions/list-integrations.md) | GET |  |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Events To Metrics Limits](actions/get-events-to-metrics-limits.md) | GET |  |
| [List Events To Metrics](actions/list-events-to-metrics.md) | GET |  |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Policies](actions/get-company-policies.md) | GET |  |
| [Get Policy Priority Settings](actions/get-policy-priority-settings.md) | GET |  |

### Retention Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Retentions](actions/get-retentions.md) | GET |  |
| [Get Retentions Enabled](actions/get-retentions-enabled.md) | GET |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Roles](actions/list-custom-roles.md) | GET |  |
| [List System Roles](actions/list-system-roles.md) | GET |  |

### Router

| Action | Method | Description |
| --- | --- | --- |
| [List Global Routers](actions/list-global-routers.md) | GET |  |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Get Quota Allocation Rule Set](actions/get-quota-allocation-rule-set.md) | GET |  |
| [List Parsing Rule Groups](actions/list-parsing-rule-groups.md) | GET |  |
| [List Recording Rules](actions/list-recording-rules.md) | GET |  |

### Scope

| Action | Method | Description |
| --- | --- | --- |
| [List Team Scopes](actions/list-team-scopes.md) | GET |  |

### Security Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Company IP Access Settings](actions/get-company-ip-access-settings.md) | GET |  |

### Slo

| Action | Method | Description |
| --- | --- | --- |
| [List SLOs](actions/list-sl-os.md) | GET |  |

### Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Usage Export Status](actions/get-data-usage-export-status.md) | GET |  |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Outgoing Webhooks](actions/list-outgoing-webhooks.md) | GET |  |

