# Satori Cyber: Native API Reference

A consolidated summary of Satori Cyber's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://app.satoricyber.com/docs/api
- **OpenAPI specification:** https://app.satoricyber.com/api/api-portal/satori_api.yaml
- **API base URL:** `https://app.satoricyber.com`

## Authentication

### Satori API Token (Bearer)

Bearer token authentication for Satori REST API (OpenAPI BearerAuth).

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.satoricyber.com/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Attributes](actions/get-account-attributes.md) | `GET /api/accounts/:accountId/attributes` | [docs](https://app.satoricyber.com/docs/api) |
| [Get Alert](actions/get-alert.md) | `GET /api/v1/alert/:id` | [docs](https://app.satoricyber.com/docs/api) |
| [Get Authorization Analytics Metrics](actions/get-authorization-analytics-metrics.md) | `GET /api/v1/authorization-analytics/:accountId/metrics` | [docs](https://app.satoricyber.com/docs/api) |
| [Get Dataset Access Details](actions/get-dataset-access-details.md) | `GET /api/v1/dataset/:datasetId/access-details` | [docs](https://app.satoricyber.com/docs/api) |
| [Get Dataset Connection Details](actions/get-dataset-connection-details.md) | `GET /api/v1/dataset/:datasetId/connection-details` | [docs](https://app.satoricyber.com/docs/api) |
| [Get Datastore State](actions/get-datastore-state.md) | `GET /api/v1/datastore/:accountId/state` | [docs](https://app.satoricyber.com/docs/api) |
| [Get Discovered Datastore Count](actions/get-discovered-datastore-count.md) | `GET /api/v1/discovered-data-stores/count` | [docs](https://app.satoricyber.com/docs/api) |
| [Get Security Policy Statistics](actions/get-security-policy-statistics.md) | `GET /api/v1/security-policies/statistics` | [docs](https://app.satoricyber.com/docs/api) |
| [List Account Environments](actions/list-account-environments.md) | `GET /api/accounts/:accountId/environments` | [docs](https://app.satoricyber.com/docs/api) |
| [List Account Roles](actions/list-account-roles.md) | `GET /api/accounts/:accountId/roles` | [docs](https://app.satoricyber.com/docs/api) |
| [List Custom Taxonomy](actions/list-custom-taxonomy.md) | `GET /api/v1/taxonomy/custom` | [docs](https://app.satoricyber.com/docs/api) |
| [List Data Access Rule History](actions/list-data-access-rule-history.md) | `GET /api/v1/data-access-rule/history` | [docs](https://app.satoricyber.com/docs/api) |
| [List Data Access Rules Overview](actions/list-data-access-rules-overview.md) | `GET /api/v1/data-access-rule/overview` | [docs](https://app.satoricyber.com/docs/api) |
| [List Datastores](actions/list-datastores.md) | `GET /api/v1/datastore` | [docs](https://app.satoricyber.com/docs/api) |
| [List Directory Groups](actions/list-directory-groups.md) | `GET /api/v1/directory/group` | [docs](https://app.satoricyber.com/docs/api) |
| [List Satori Taxonomy](actions/list-satori-taxonomy.md) | `GET /api/v1/taxonomy/satori` | [docs](https://app.satoricyber.com/docs/api) |
| [List Service Account Roles](actions/list-service-account-roles.md) | `GET /api/service-accounts/:serviceAccountId/roles` | [docs](https://app.satoricyber.com/docs/api) |
| [Search Alerts](actions/search-alerts.md) | `GET /api/v1/alert` | [docs](https://app.satoricyber.com/docs/api) |
| [Search Atlas Clusters](actions/search-atlas-clusters.md) | `GET /api/v1/authorization-analytics/search-atlas-clusters` | [docs](https://app.satoricyber.com/docs/api) |
| [Search Authorization Analytics](actions/search-authorization-analytics.md) | `GET /api/v1/authorization-analytics/:accountId/query` | [docs](https://app.satoricyber.com/docs/api) |
| [Search AWS Accounts](actions/search-aws-accounts.md) | `GET /api/v1/authorization-analytics/search-aws-accounts` | [docs](https://app.satoricyber.com/docs/api) |
| [Search Datasets](actions/search-datasets.md) | `GET /api/v1/dataset` | [docs](https://app.satoricyber.com/docs/api) |
| [Search Directory Group Suggestions](actions/search-directory-group-suggestions.md) | `GET /api/v1/directory/ui/groups/suggestions` | [docs](https://app.satoricyber.com/docs/api) |
| [Search Directory Member Suggestions](actions/search-directory-member-suggestions.md) | `GET /api/v1/directory/ui/members/suggestions` | [docs](https://app.satoricyber.com/docs/api) |
| [Search GCP Projects](actions/search-gcp-projects.md) | `GET /api/v1/authorization-analytics/search-gcp-projects` | [docs](https://app.satoricyber.com/docs/api) |
