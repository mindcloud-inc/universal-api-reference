# <img src="https://images.mindcloud.co/apps/icons/download-3_1775832140632.jpeg" alt="InfluxDB Cloud logo" width="28" height="28"> InfluxDB Cloud: Universal API

InfluxDB Cloud is InfluxData's managed time series database and API for buckets, organizations, users, tasks, labels, authorizations, and related administration endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/influxDBCloud/latest
- **Category:** IT Operations / Database
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.influxdata.com/products/influxdb-cloud/
- **Vendor API docs:** https://docs.influxdata.com/influxdb/cloud/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Buckets](actions/list-buckets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-buckets?connectionId=$CONNECTION_ID&orgId=%7B%7Bcredentials.orgId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Authorization](actions/get-authorization.md) | GET | Retrieves an authorization from InfluxDB Cloud. |
| [List Authorizations](actions/list-authorizations.md) | GET | Retrieves authorizations from InfluxDB Cloud. |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from InfluxDB Cloud. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Bucket](actions/get-bucket.md) | GET | Retrieves a bucket from InfluxDB Cloud. |
| [List Buckets](actions/list-buckets.md) | GET | Retrieves buckets from InfluxDB Cloud. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from InfluxDB Cloud. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Get Bucket Labels](actions/get-bucket-labels.md) | GET | Retrieves bucket labels from InfluxDB Cloud. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from InfluxDB Cloud. |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [List Telegrafs](actions/list-telegrafs.md) | GET | Retrieves Telegrafs from InfluxDB Cloud. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from InfluxDB Cloud. |
| [Get Organization Limits](actions/get-organization-limits.md) | GET | Retrieves organization limits from InfluxDB Cloud. |
| [Get Organization Usage](actions/get-organization-usage.md) | GET | Retrieves organization usage from InfluxDB Cloud. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from InfluxDB Cloud. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Secrets](actions/get-organization-secrets.md) | GET | Retrieves organization secrets from InfluxDB Cloud. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Flags](actions/get-flags.md) | GET | Retrieves feature flags from InfluxDB Cloud. |
| [Get Query Suggestions](actions/get-query-suggestions.md) | GET | Retrieves query suggestions from InfluxDB Cloud. |
| [Get Setup Status](actions/get-setup-status.md) | GET | Retrieves setup status from InfluxDB Cloud. |
| [List Checks](actions/list-checks.md) | GET | Retrieves checks from InfluxDB Cloud. |
| [List Notification Endpoints](actions/list-notification-endpoints.md) | GET | Retrieves notification endpoints from InfluxDB Cloud. |
| [List Notification Rules](actions/list-notification-rules.md) | GET | Retrieves notification rules from InfluxDB Cloud. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from InfluxDB Cloud. |
| [List Variables](actions/list-variables.md) | GET | Retrieves variables from InfluxDB Cloud. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Bucket Members](actions/get-bucket-members.md) | GET | Retrieves bucket members from InfluxDB Cloud. |
| [Get Bucket Owners](actions/get-bucket-owners.md) | GET | Retrieves bucket owners from InfluxDB Cloud. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from InfluxDB Cloud. |
| [Get Organization Members](actions/get-organization-members.md) | GET | Retrieves organization members from InfluxDB Cloud. |
| [Get Organization Owners](actions/get-organization-owners.md) | GET | Retrieves organization owners from InfluxDB Cloud. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from InfluxDB Cloud. |
| [List Users](actions/list-users.md) | GET | Retrieves users from InfluxDB Cloud. |

