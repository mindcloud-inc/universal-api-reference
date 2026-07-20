# DevCycle: Native API Reference

A consolidated summary of DevCycle's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://docs.devcycle.com/management-api/
- **OpenAPI specification:** https://api.devcycle.com/openapi.json
- **API base URL:** `https://api.devcycle.com`

## Authentication

### DevCycle OAuth2

OAuth2 client-credentials auth for the DevCycle Management API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.devcycle.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.devcycle.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.devcycle.com/management-api/)

## Pagination

Use `perPage` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Custom Property](actions/get-custom-property.md) | `GET /v1/projects/:project/customProperties/:key` | [docs](https://docs.devcycle.com/management-api/#tag/Custom-Properties/operation/CustomPropertiesController_findOne) |
| [Get Dynatrace Integration](actions/get-dynatrace-integration.md) | `GET /v1/integrations/dynatrace` | [docs](https://docs.devcycle.com/management-api/#tag/Integrations:-Dynatrace/operation/DynatraceIntegrationController_getIntegrations) |
| [Get Environment](actions/get-environment.md) | `GET /v1/projects/:project/environments/:key` | [docs](https://docs.devcycle.com/management-api/#tag/Environments/operation/EnvironmentsController_findOne) |
| [Get Feature](actions/get-feature.md) | `GET /v2/projects/:project/features/:feature` | [docs](https://docs.devcycle.com/management-api/#tag/Features-v2/operation/FeaturesController_findOne) |
| [Get Feature Overrides](actions/get-feature-overrides.md) | `GET /v1/projects/:project/features/:feature/overrides` | [docs](https://docs.devcycle.com/management-api/#tag/Overrides/operation/OverridesController_findOverridesForFeature) |
| [Get Feature Staleness](actions/get-feature-staleness.md) | `GET /v2/projects/:project/features/:feature/staleness` | [docs](https://docs.devcycle.com/management-api/#tag/Features-v2/operation/FeaturesController_getStaleness) |
| [Get Feature Total Evaluations](actions/get-feature-total-evaluations.md) | `GET /v1/projects/:project/features/:feature/results/total-evaluations` | [docs](https://docs.devcycle.com/management-api/#tag/Results/operation/ResultsController_getTotalEvaluationsPerHourByFeature) |
| [Get Feature Variation](actions/get-feature-variation.md) | `GET /v1/projects/:project/features/:feature/variations/:key` | [docs](https://docs.devcycle.com/management-api/#tag/Variations/operation/VariationsController_findOne) |
| [Get Metric](actions/get-metric.md) | `GET /v1/projects/:project/metrics/:key` | [docs](https://docs.devcycle.com/management-api/#tag/Metrics/operation/MetricsController_findOne) |
| [Get Metric Results](actions/get-metric-results.md) | `GET /v1/projects/:project/metrics/:key/results` | [docs](https://docs.devcycle.com/management-api/#tag/Metrics/operation/MetricsController_fetchResults) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/:key` | [docs](https://docs.devcycle.com/management-api/#tag/Projects/operation/ProjectsController_findOne) |
| [Get Project Evaluations](actions/get-project-evaluations.md) | `GET /v1/projects/:project/results/evaluations` | [docs](https://docs.devcycle.com/management-api/#tag/Results/operation/ResultsController_getEvaluationsPerHourByProject) |
| [Get Project Total Evaluations](actions/get-project-total-evaluations.md) | `GET /v1/projects/:project/results/total-evaluations` | [docs](https://docs.devcycle.com/management-api/#tag/Results/operation/ResultsController_getTotalEvaluationsPerHourByProject) |
| [Get Test Metric Results](actions/get-test-metric-results.md) | `GET /v1/projects/:project/test-metric-results` | [docs](https://docs.devcycle.com/management-api/#tag/Metrics/operation/TestMetricResultsController_fetch) |
| [Get Variable](actions/get-variable.md) | `GET /v1/projects/:project/variables/:key` | [docs](https://docs.devcycle.com/management-api/#tag/Variables/operation/VariablesController_findOne) |
| [List Audiences](actions/list-audiences.md) | `GET /v1/projects/:project/audiences` | [docs](https://docs.devcycle.com/management-api/#tag/Audiences/operation/AudiencesController_findAll) |
| [List Custom Properties](actions/list-custom-properties.md) | `GET /v1/projects/:project/customProperties` | [docs](https://docs.devcycle.com/management-api/#tag/Custom-Properties/operation/CustomPropertiesController_findAll) |
| [List Environments](actions/list-environments.md) | `GET /v1/projects/:project/environments` | [docs](https://docs.devcycle.com/management-api/#tag/Environments/operation/EnvironmentsController_findAll) |
| [List Feature Audit Entries](actions/list-feature-audit-entries.md) | `GET /v1/projects/:project/features/:feature/audit` | [docs](https://docs.devcycle.com/management-api/#tag/Audit-Log/operation/AuditLogController_findAll) |
| [List Feature Configurations](actions/list-feature-configurations.md) | `GET /v1/projects/:project/features/:feature/configurations` | [docs](https://docs.devcycle.com/management-api/#tag/Feature-Configurations/operation/FeatureConfigsController_findAll) |
| [List Feature Variations](actions/list-feature-variations.md) | `GET /v1/projects/:project/features/:feature/variations` | [docs](https://docs.devcycle.com/management-api/#tag/Variations/operation/VariationsController_findAll) |
| [List Features](actions/list-features.md) | `GET /v2/projects/:project/features` | [docs](https://docs.devcycle.com/management-api/#tag/Features-v2/operation/FeaturesController_findAll) |
| [List Linked Jira Issues](actions/list-linked-jira-issues.md) | `GET /v1/projects/:project/features/:feature/integrations/jira/issues` | [docs](https://docs.devcycle.com/management-api/#tag/Deprecated-Features-v1/operation/FeaturesController_findAllLinkedIssues_v1) |
| [List Metric Associations](actions/list-metric-associations.md) | `GET /v1/projects/:project/metric-associations` | [docs](https://docs.devcycle.com/management-api/#tag/Metric-Associations/operation/MetricAssociationsController_findAll) |
| [List Metrics](actions/list-metrics.md) | `GET /v1/projects/:project/metrics` | [docs](https://docs.devcycle.com/management-api/#tag/Metrics/operation/MetricsController_findAll) |
| [List Project Stale Features](actions/list-project-stale-features.md) | `GET /v1/projects/:key/staleness` | [docs](https://docs.devcycle.com/management-api/#tag/Projects/operation/ProjectsController_getStaleness) |
| [List Projects](actions/list-projects.md) | `GET /v1/projects` | [docs](https://docs.devcycle.com/management-api/#tag/Projects/operation/ProjectsController_findAll) |
| [List Variables](actions/list-variables.md) | `GET /v1/projects/:project/variables` | [docs](https://docs.devcycle.com/management-api/#tag/Variables/operation/VariablesController_findAll) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/projects/:project/webhooks` | [docs](https://docs.devcycle.com/management-api/#tag/Webhooks/operation/WebhooksController_findAll) |
