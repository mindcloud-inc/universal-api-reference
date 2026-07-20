# Conversion Tools: Update Task Retention

Updates an existing task retention mode in Conversion Tools.

```
PUT https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/update-task-retention
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conversion Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/update-task-retention" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "28f2f333593949fe9b33c859c6d339de",
  "retentionMode": "standard_24h"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/update-task-retention', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "28f2f333593949fe9b33c859c6d339de",
    "retentionMode": "standard_24h"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The task ID to update. Example: `28f2f333593949fe9b33c859c6d339de`. |
| `retentionMode` | list<string> | yes | Retention mode to apply to the task files. `ttl_15m` is only available on paid Conversion Tools plans. One of: `standard_24h`, `ttl_15m`. Default: `standard_24h`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateExpires": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "retentionMode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateExpires` | date | When the provider plans to delete the task files. |
| `error` | string | Provider error message when present. |
| `retentionMode` | string | Applied task retention mode. |

## Native endpoint

Through the native Conversion Tools API, this operation is `PATCH /tasks/:taskId/retention` (base URL `https://api.conversiontools.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-retention.md) for the provider-specific parameters and requirements.

