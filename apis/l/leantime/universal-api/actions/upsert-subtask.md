# Leantime: Upsert Subtask



```
PUT https://connect.mindcloud.co/v1/universal/leantime/latest/actions/upsert-subtask
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/upsert-subtask" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.values.headline": "string",
  "params.values.status": "3",
  "params.parentTicket.id": 1,
  "params.parentTicket.projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/upsert-subtask', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.values.headline": "string",
    "params.values.status": "3",
    "params.parentTicket.id": 1,
    "params.parentTicket.projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.values.headline` | string | yes |  |
| `params.values.status` | number | yes | Default: `3`. |
| `params.values.description` | string | no |  |
| `params.values.subtaskId` | number | no |  |
| `params.parentTicket.id` | number | yes |  |
| `params.parentTicket.projectId` | number | yes |  |
| `params.parentTicket.milestoneid` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-subtask.md) for the provider-specific parameters and requirements.

