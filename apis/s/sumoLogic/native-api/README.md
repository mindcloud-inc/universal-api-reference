# Sumo Logic: Native API Reference

A consolidated summary of Sumo Logic's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.sumologic.com/help/docs/api/
- **OpenAPI specification:** https://api.sumologic.com/docs/sumologic-api.yaml
- **API base URL:** `https://api.sumologic.com/api`

## Authentication

### Basic Authentication

Authenticate Sumo Logic API requests with HTTP Basic auth using the Sumo Logic Access ID as the username and Access Key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.sumologic.com/help/docs/api/about-apis/getting-started/)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `token` in the query string as the pagination cursor; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sortBy` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Access Keys](actions/list-access-keys.md) | `GET /v1/accessKeys` | [docs](https://api.sumologic.com/docs/#/accessKeyManagement/listAccessKeys) |
| [List Apps](actions/list-apps.md) | `GET /v1/apps` | [docs](https://api.sumologic.com/docs/#/appManagement/listApps) |
| [List Apps V2](actions/list-apps-v2.md) | `GET /v2/apps` | [docs](https://api.sumologic.com/docs/#/appManagementV2/listAppsV2) |
| [List Built-In Fields](actions/list-built-in-fields.md) | `GET /v1/fields/builtin` | [docs](https://api.sumologic.com/docs/#/fieldManagementV1/listBuiltInFields) |
| [List Connections](actions/list-connections.md) | `GET /v1/connections` | [docs](https://api.sumologic.com/docs/#/connectionManagement/listConnections) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /v1/fields` | [docs](https://api.sumologic.com/docs/#/fieldManagementV1/listCustomFields) |
| [List Data Deletion Rules](actions/list-data-deletion-rules.md) | `GET /v1/dataDeletionRules` | [docs](https://api.sumologic.com/docs/#/dataDeletionRules/listDeletionRules) |
| [List Data Masking Rules](actions/list-data-masking-rules.md) | `GET /v1/dataMaskingRules` | [docs](https://api.sumologic.com/docs/#/dataMaskingManagement/listDataMaskingRules) |
| [List Dropped Fields](actions/list-dropped-fields.md) | `GET /v1/fields/dropped` | [docs](https://api.sumologic.com/docs/#/fieldManagementV1/listDroppedFields) |
| [List Dynamic Parsing Rules](actions/list-dynamic-parsing-rules.md) | `GET /v1/dynamicParsingRules` | [docs](https://api.sumologic.com/docs/#/dynamicParsingRuleManagement/listDynamicParsingRules) |
| [List Field Extraction Rules](actions/list-field-extraction-rules.md) | `GET /v1/extractionRules` | [docs](https://api.sumologic.com/docs/#/extractionRuleManagement/listExtractionRules) |
| [List Health Events](actions/list-health-events.md) | `GET /v1/healthEvents` | [docs](https://api.sumologic.com/docs/#/healthEvents/listAllHealthEvents) |
| [List Ingest Budgets](actions/list-ingest-budgets.md) | `GET /v2/ingestBudgets` | [docs](https://api.sumologic.com/docs/#/ingestBudgetManagementV2/listIngestBudgetsV2) |
| [List Log Data Forwarding Rules](actions/list-log-data-forwarding-rules.md) | `GET /v1/logsDataForwarding/rules` | [docs](https://api.sumologic.com/docs/#/logsDataForwardingManagement/getRulesAndBuckets) |
| [List Log Searches](actions/list-log-searches.md) | `GET /v1/logSearches` | [docs](https://api.sumologic.com/docs/#/logSearchesManagement/listLogSearches) |
| [List Partitions](actions/list-partitions.md) | `GET /v1/partitions` | [docs](https://api.sumologic.com/docs/#/partitionManagement/listPartitions) |
| [List Personal Access Keys](actions/list-personal-access-keys.md) | `GET /v1/accessKeys/personal` | [docs](https://api.sumologic.com/docs/#/accessKeyManagement/listPersonalAccessKeys) |
| [List Roles](actions/list-roles.md) | `GET /v1/roles` | [docs](https://api.sumologic.com/docs/#/roleManagement/listRoles) |
| [List Roles V2](actions/list-roles-v2.md) | `GET /v2/roles` | [docs](https://api.sumologic.com/docs/#/roleManagementV2/listRolesV2) |
| [List Scheduled Views](actions/list-scheduled-views.md) | `GET /v1/scheduledViews` | [docs](https://api.sumologic.com/docs/#/scheduledViewManagement/listScheduledViews) |
| [List Service Accounts](actions/list-service-accounts.md) | `GET /v1/serviceAccounts` | [docs](https://api.sumologic.com/docs/#/serviceAccountManagement/listServiceAccounts) |
| [List Tokens](actions/list-tokens.md) | `GET /v1/tokens` | [docs](https://api.sumologic.com/docs/#/tokensLibraryManagement/listTokens) |
| [List Transformation Rules](actions/list-transformation-rules.md) | `GET /v1/transformationRules` | [docs](https://api.sumologic.com/docs/#/transformationRuleManagement/getTransformationRules) |
| [List Users](actions/list-users.md) | `GET /v1/users` | [docs](https://api.sumologic.com/docs/#/userManagement/listUsers) |
