# <img src="https://images.mindcloud.co/apps/icons/clickhouse-original-512px_1776375098232.png" alt="ClickHouse logo" width="28" height="28"> ClickHouse: Universal API

ClickHouse Cloud is a managed analytical database platform for creating, managing, monitoring, and securing ClickHouse services and related cloud resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clickHouse/latest
- **Category:** IT Operations / Database
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clickhouse.com
- **Vendor API docs:** https://clickhouse.com/docs/cloud/manage/api/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organizations](actions/get-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET |  |
| [List Activities](actions/list-activities.md) | GET |  |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key](actions/get-api-key.md) | GET |  |
| [List API Keys](actions/list-api-keys.md) | GET |  |

### Backup

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Backup](actions/get-service-backup.md) | GET |  |
| [List Service Backups](actions/list-service-backups.md) | GET |  |

### Backup Bucket

| Action | Method | Description |
| --- | --- | --- |
| [Get Backup Bucket](actions/get-backup-bucket.md) | GET |  |

### Backup Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Backup Configuration](actions/get-backup-configuration.md) | GET |  |

### Clickpipe

| Action | Method | Description |
| --- | --- | --- |
| [Get ClickPipe](actions/get-click-pipe.md) | GET |  |
| [List ClickPipes](actions/list-click-pipes.md) | GET |  |

### Clickpipe Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get ClickPipe Settings](actions/get-click-pipe-settings.md) | GET |  |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Private Endpoint Configuration](actions/get-private-endpoint-configuration.md) | GET |  |
| [Get Service Query Endpoint](actions/get-service-query-endpoint.md) | GET |  |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Get Invitation](actions/get-invitation.md) | GET |  |
| [List Invitations](actions/list-invitations.md) | GET |  |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Metrics](actions/get-organization-metrics.md) | GET |  |
| [Get Service Metrics](actions/get-service-metrics.md) | GET |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [Get Organizations](actions/get-organizations.md) | GET |  |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET |  |
| [List Services](actions/list-services.md) | GET |  |

### Usage Cost

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage Costs](actions/get-usage-costs.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Member](actions/get-organization-member.md) | GET |  |
| [List Organization Members](actions/list-organization-members.md) | GET |  |

