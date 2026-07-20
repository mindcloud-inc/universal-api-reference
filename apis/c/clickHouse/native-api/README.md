# ClickHouse: Native API Reference

A consolidated summary of ClickHouse's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://clickhouse.com/docs/cloud/manage/api/api-overview
- **OpenAPI specification:** https://api.clickhouse.cloud/v1
- **API base URL:** `https://api.clickhouse.cloud`

## Authentication

### ClickHouse Cloud API Key

Use your ClickHouse Cloud API Key ID as the username and API Key Secret as the password.

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

[Official authentication documentation](https://clickhouse.com/docs/cloud/manage/openapi)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | `GET /v1/organizations/[:organizationId]/activities/[:activityId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get API Key](actions/get-api-key.md) | `GET /v1/organizations/[:organizationId]/keys/[:keyId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Backup Bucket](actions/get-backup-bucket.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/backupBucket` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Backup Configuration](actions/get-backup-configuration.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/backupConfiguration` | [docs](https://api.clickhouse.cloud/v1) |
| [Get ClickPipe](actions/get-click-pipe.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/clickpipes/[:clickPipeId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get ClickPipe Settings](actions/get-click-pipe-settings.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/clickpipes/[:clickPipeId]/settings` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Invitation](actions/get-invitation.md) | `GET /v1/organizations/[:organizationId]/invitations/[:invitationId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Organization](actions/get-organization.md) | `GET /v1/organizations/[:organizationId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Organization Member](actions/get-organization-member.md) | `GET /v1/organizations/[:organizationId]/members/[:userId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Organization Metrics](actions/get-organization-metrics.md) | `GET /v1/organizations/[:organizationId]/prometheus` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Organizations](actions/get-organizations.md) | `GET /v1/organizations` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Private Endpoint Configuration](actions/get-private-endpoint-configuration.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/privateEndpointConfig` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Service](actions/get-service.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Service Backup](actions/get-service-backup.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/backups/[:backupId]` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Service Metrics](actions/get-service-metrics.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/prometheus` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Service Query Endpoint](actions/get-service-query-endpoint.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/serviceQueryEndpoint` | [docs](https://api.clickhouse.cloud/v1) |
| [Get Usage Costs](actions/get-usage-costs.md) | `GET /v1/organizations/[:organizationId]/usageCost` | [docs](https://api.clickhouse.cloud/v1) |
| [List Activities](actions/list-activities.md) | `GET /v1/organizations/[:organizationId]/activities` | [docs](https://api.clickhouse.cloud/v1) |
| [List API Keys](actions/list-api-keys.md) | `GET /v1/organizations/[:organizationId]/keys` | [docs](https://api.clickhouse.cloud/v1) |
| [List ClickPipes](actions/list-click-pipes.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/clickpipes` | [docs](https://api.clickhouse.cloud/v1) |
| [List Invitations](actions/list-invitations.md) | `GET /v1/organizations/[:organizationId]/invitations` | [docs](https://api.clickhouse.cloud/v1) |
| [List Organization Members](actions/list-organization-members.md) | `GET /v1/organizations/[:organizationId]/members` | [docs](https://api.clickhouse.cloud/v1) |
| [List Service Backups](actions/list-service-backups.md) | `GET /v1/organizations/[:organizationId]/services/[:serviceId]/backups` | [docs](https://api.clickhouse.cloud/v1) |
| [List Services](actions/list-services.md) | `GET /v1/organizations/[:organizationId]/services` | [docs](https://api.clickhouse.cloud/v1) |
