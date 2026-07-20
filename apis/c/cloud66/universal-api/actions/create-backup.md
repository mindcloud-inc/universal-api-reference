# Cloud 66: Create Backup

Creates a backup for a Cloud 66 stack.

```
POST https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/create-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/create-backup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/create-backup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes | The stack UID. |
| `dbType` | string | no | Comma-separated database types to back up. |
| `frequency` | string | no | Cron schedule for the backup task. |
| `keepCount` | number | no | Number of previous backups to keep. |
| `gzip` | boolean | no | Whether to gzip the backup. |
| `excludedTables` | string | no | Tables to exclude from the backup. |
| `runOnReplicaServer` | boolean | no | Run the backup on a replica server when available. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `POST /stacks/:stack_id/backups` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-backup.md) for the provider-specific parameters and requirements.

