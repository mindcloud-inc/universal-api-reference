# ClickHouse: List Service Backups



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-service-backups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-service-backups?connectionId=$CONNECTION_ID&organizationId=string&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-service-backups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | ID of the organization that owns the service. |
| `serviceId` | string | yes | ID of the requested service. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backupName": "Ava Chen",
      "bucket": {},
      "durationInSeconds": 1,
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "serviceId": "string",
      "sizeInBytes": 1,
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backupName` | string | Backup name on the external backup bucket. |
| `bucket` | object | Backup bucket where the backup is stored. |
| `durationInSeconds` | number | Backup duration in seconds. |
| `finishedAt` | date | Backup finish timestamp. |
| `id` | string | Unique backup ID. |
| `serviceId` | string | Service ID associated with the backup. |
| `sizeInBytes` | number | Backup size in bytes. |
| `startedAt` | date | Backup start timestamp. |
| `status` | string | Backup status. |
| `type` | string | Backup type. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/services/[:serviceId]/backups` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-backups.md) for the provider-specific parameters and requirements.

