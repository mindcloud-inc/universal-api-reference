# Coralogix: Native API Reference

A consolidated summary of Coralogix's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://docs.coralogix.com/
- **OpenAPI specification:** https://api.coralogix.com/mgmt/openapi/latest/openapi.yaml
- **API base URL:** `https://api.eu2.coralogix.com/mgmt/openapi/latest`

## Authentication

### API Key

Connect with a Coralogix user or team API key for the EU2 region.

### Credentials

- **Coralogix API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.coralogix.com/api-reference/latest/api-keys-service/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Alert Filter Option Counts](actions/get-alert-filter-option-counts.md) | `GET /alerts/alerts-general/v3/filter-option-counts` | [docs](https://docs.coralogix.com/api-reference/latest/alert-definitions-service/filter-option-counts) |
| [Get Company Enrichment Settings](actions/get-company-enrichment-settings.md) | `GET /enrichment-rules/enrichment-rules/v1/settings` | [docs](https://docs.coralogix.com/api-reference/latest/enrichments-service/get-company-enrichment-settings) |
| [Get Company IP Access Settings](actions/get-company-ip-access-settings.md) | `GET /aaa/team-sec-ip-access/v1` | [docs](https://docs.coralogix.com/api-reference/latest/ip-access-service/get-company-ip-access-settings) |
| [Get Company Policies](actions/get-company-policies.md) | `GET /dataplans/policies/v1` | [docs](https://docs.coralogix.com/api-reference/latest/policies-service/get-company-policies) |
| [Get Connector Type Summaries](actions/get-connector-type-summaries.md) | `GET /notifications/notification-center/v1/connectors:getTypeSummaries` | [docs](https://docs.coralogix.com/api-reference/latest/connectors-service/get-connector-type-summaries) |
| [Get Dashboard Catalog](actions/get-dashboard-catalog.md) | `GET /dashboards/dashboards/v1/catalog` | [docs](https://docs.coralogix.com/api-reference/latest/dashboard-service/get-dashboard-catalog) |
| [Get Data Usage Export Status](actions/get-data-usage-export-status.md) | `GET /dataplans/data-usage/v2/export-status` | [docs](https://docs.coralogix.com/api-reference/latest/data-usage-service/get-data-usage-metrics-export-status) |
| [Get Enrichment Limit](actions/get-enrichment-limit.md) | `GET /enrichment-rules/enrichment-rules/v1/limit` | [docs](https://docs.coralogix.com/api-reference/latest/enrichments-service/get-enrichment-limit) |
| [Get Events To Metrics Limits](actions/get-events-to-metrics-limits.md) | `GET /events2metrics/events2metrics/v2/limits` | [docs](https://docs.coralogix.com/api-reference/latest/events2metrics-service/get-limits) |
| [Get Logs Archive Target](actions/get-logs-archive-target.md) | `GET /logs/data-setup/v2` | [docs](https://docs.coralogix.com/api-reference/latest/target-service/get-target) |
| [Get Policy Priority Settings](actions/get-policy-priority-settings.md) | `GET /dataplans/policies/v1/getPolicyPrioritySettings` | [docs](https://docs.coralogix.com/api-reference/latest/policies-service/get-policy-settings) |
| [Get Quota Allocation Rule Set](actions/get-quota-allocation-rule-set.md) | `GET /quota-rules/v1/quota-allocation-rule-set` | [docs](https://docs.coralogix.com/api-reference/latest/quota-allocation-rules-service/get-quota-allocation-rule-set) |
| [Get Retentions](actions/get-retentions.md) | `GET /dataengine/retention-tags/v1` | [docs](https://docs.coralogix.com/api-reference/latest/retentions-service/get-retentions) |
| [Get Retentions Enabled](actions/get-retentions-enabled.md) | `GET /dataengine/retention-tags/v1/enabled` | [docs](https://docs.coralogix.com/api-reference/latest/retentions-service/get-retentions-enabled) |
| [Get System Default Case Team Config](actions/get-system-default-case-team-config.md) | `GET /cases/cases/team-configs/v1/configs/system-defaults` | [docs](https://docs.coralogix.com/api-reference/latest/team-config-service/get-system-defaults) |
| [List Alert Definitions](actions/list-alert-definitions.md) | `GET /alerts/alerts-general/v3` | [docs](https://docs.coralogix.com/api-reference/latest/alert-definitions-service/list-alert-defs) |
| [List Alert Scheduler Rules](actions/list-alert-scheduler-rules.md) | `GET /v1/alert-scheduler-rules/bulk` | [docs](https://docs.coralogix.com/api-reference/latest/alert-scheduler-rule-service/get-bulk-alert-scheduler-rule) |
| [List Connector Summaries](actions/list-connector-summaries.md) | `GET /notifications/notification-center/v1/connectors:listSummaries` | [docs](https://docs.coralogix.com/api-reference/latest/connectors-service/list-connector-summaries) |
| [List Contextual Data Integrations](actions/list-contextual-data-integrations.md) | `GET /integrations/contextual-data/v1` | [docs](https://docs.coralogix.com/api-reference/latest/contextual-data-integration-service/get-contextual-data-integrations) |
| [List Custom Enrichments](actions/list-custom-enrichments.md) | `GET /enrichment-rules/custom-enrichment-rules/v1` | [docs](https://docs.coralogix.com/api-reference/latest/custom-enrichments-service/get-custom-enrichments) |
| [List Custom Roles](actions/list-custom-roles.md) | `GET /aaa/team-roles/v1/custom-roles` | [docs](https://docs.coralogix.com/api-reference/latest/role-management-service/list-custom-roles) |
| [List Dashboard Folders](actions/list-dashboard-folders.md) | `GET /dashboards/dashboards/v1/folders` | [docs](https://docs.coralogix.com/api-reference/latest/dashboard-folders-service/list-dashboard-folders) |
| [List Deployed Extensions](actions/list-deployed-extensions.md) | `GET /integrations/extensions/v1/deployed` | [docs](https://docs.coralogix.com/api-reference/latest/extension-deployment-service/get-deployed-extensions) |
| [List Enrichments](actions/list-enrichments.md) | `GET /enrichment-rules/enrichment-rules/v1` | [docs](https://docs.coralogix.com/api-reference/latest/enrichments-service/get-enrichments) |
| [List Events To Metrics](actions/list-events-to-metrics.md) | `GET /events2metrics/events2metrics/v2` | [docs](https://docs.coralogix.com/api-reference/latest/events2metrics-service/list-e2-ms) |
| [List Global Routers](actions/list-global-routers.md) | `GET /notifications/notification-center/v1/routers` | [docs](https://docs.coralogix.com/api-reference/latest/global-routers-service/list-global-routers) |
| [List Incident Aggregations](actions/list-incident-aggregations.md) | `GET /incidents/incidents/v1/aggregations` | [docs](https://docs.coralogix.com/api-reference/latest/incidents-service/list-incident-aggregations) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations/integrations/v1` | [docs](https://docs.coralogix.com/api-reference/latest/integration-service/get-integrations) |
| [List Notification Connectors](actions/list-notification-connectors.md) | `GET /notifications/notification-center/v1/connectors` | [docs](https://docs.coralogix.com/api-reference/latest/connectors-service/list-connectors) |
| [List Notification Entity Types](actions/list-notification-entity-types.md) | `GET /notifications/notification-center/v1/entity-types` | [docs](https://docs.coralogix.com/api-reference/latest/entities-service/list-entity-types) |
| [List Outgoing Webhooks](actions/list-outgoing-webhooks.md) | `GET /integrations/webhooks/v1` | [docs](https://docs.coralogix.com/api-reference/latest/outgoing-webhooks-service/list-all-outgoing-webhooks) |
| [List Parsing Rule Groups](actions/list-parsing-rule-groups.md) | `GET /parsing-rules/rule-groups/v1` | [docs](https://docs.coralogix.com/api-reference/latest/rule-groups-service/list-rule-groups) |
| [List Recording Rules](actions/list-recording-rules.md) | `GET /v1/rule-group-sets` | [docs](https://docs.coralogix.com/api-reference/latest/recording-rules-service/list) |
| [List Send Data API Keys](actions/list-send-data-api-keys.md) | `GET /aaa/api-keys/v3/send_data` | [docs](https://docs.coralogix.com/api-reference/latest/api-keys-service/get-send-data-api-keys) |
| [List SLOs](actions/list-sl-os.md) | `GET /v1/slo/slos` | [docs](https://docs.coralogix.com/api-reference/latest/slos-service/list-slos) |
| [List System Roles](actions/list-system-roles.md) | `GET /aaa/team-roles/v1/system-roles` | [docs](https://docs.coralogix.com/api-reference/latest/role-management-service/list-system-roles) |
| [List Team Scopes](actions/list-team-scopes.md) | `GET /aaa/team-scopes/v1/list` | [docs](https://docs.coralogix.com/api-reference/latest/scopes-service/get-team-scopes) |
| [List View Folders](actions/list-view-folders.md) | `GET /data-exploration/saved-views/v1/folders` | [docs](https://docs.coralogix.com/api-reference/latest/folders-for-views-service/list-view-folders-service) |
| [List Views](actions/list-views.md) | `GET /data-exploration/saved-views/v1` | [docs](https://docs.coralogix.com/api-reference/latest/views-service/list-views-service) |
