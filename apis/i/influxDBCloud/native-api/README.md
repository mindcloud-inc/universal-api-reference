# InfluxDB Cloud: Native API Reference

A consolidated summary of InfluxDB Cloud's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://docs.influxdata.com/influxdb/cloud/api/
- **API base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`

## Authentication

### API Key

Use an InfluxDB Cloud API token for authenticated requests to the cluster-specific v2 API.

### Credentials

- **API Key:** `apiKey` · required
- **Organization ID:** `orgId` · optional · InfluxDB Cloud organization ID used by many v2 API endpoints and connection checks.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.influxdata.com/influxdb/cloud/admin/tokens/use-tokens/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Authorization](actions/get-authorization.md) | `GET /authorizations/:authID` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetAuthorizationsID) |
| [Get Bucket](actions/get-bucket.md) | `GET /buckets/:bucketID` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsID) |
| [Get Bucket Labels](actions/get-bucket-labels.md) | `GET /buckets/:bucketID/labels` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsIDLabels) |
| [Get Bucket Members](actions/get-bucket-members.md) | `GET /buckets/:bucketID/members` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsIDMembers) |
| [Get Bucket Owners](actions/get-bucket-owners.md) | `GET /buckets/:bucketID/owners` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsIDOwners) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetMe) |
| [Get Flags](actions/get-flags.md) | `GET /flags` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetFlags) |
| [Get Organization](actions/get-organization.md) | `GET /orgs/:orgID` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgsID) |
| [Get Organization Limits](actions/get-organization-limits.md) | `GET /orgs/:orgID/limits` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgLimitsID) |
| [Get Organization Members](actions/get-organization-members.md) | `GET /orgs/:orgID/members` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgsIDMembers) |
| [Get Organization Owners](actions/get-organization-owners.md) | `GET /orgs/:orgID/owners` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgsIDOwners) |
| [Get Organization Secrets](actions/get-organization-secrets.md) | `GET /orgs/:orgID/secrets` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgsIDSecrets) |
| [Get Organization Usage](actions/get-organization-usage.md) | `GET /orgs/:orgID/usage` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgUsageID) |
| [Get Query Suggestions](actions/get-query-suggestions.md) | `GET /query/suggestions` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetQuerySuggestions) |
| [Get Setup Status](actions/get-setup-status.md) | `GET /setup` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetSetup) |
| [Get User](actions/get-user.md) | `GET /users/:userID` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetUsersID) |
| [List Authorizations](actions/list-authorizations.md) | `GET /authorizations` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetAuthorizations) |
| [List Buckets](actions/list-buckets.md) | `GET /buckets` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBuckets) |
| [List Checks](actions/list-checks.md) | `GET /checks` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetChecks) |
| [List Dashboards](actions/list-dashboards.md) | `GET /dashboards` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetDashboards) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetLabels) |
| [List Notification Endpoints](actions/list-notification-endpoints.md) | `GET /notificationEndpoints` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetNotificationEndpoints) |
| [List Notification Rules](actions/list-notification-rules.md) | `GET /notificationRules` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetNotificationRules) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgs) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetResources) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetTasks) |
| [List Telegrafs](actions/list-telegrafs.md) | `GET /telegrafs` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetTelegrafs) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetUsers) |
| [List Variables](actions/list-variables.md) | `GET /variables` | [docs](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetVariables) |
