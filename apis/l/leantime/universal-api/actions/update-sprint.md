# Leantime: Update Sprint



```
PUT https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-sprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.params.id": 1,
  "params.params.name": "Ava Chen",
  "params.params.projectId": 1,
  "params.params.startDate": "string",
  "params.params.endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-sprint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.params.id": 1,
    "params.params.name": "Ava Chen",
    "params.params.projectId": 1,
    "params.params.startDate": "string",
    "params.params.endDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.params.id` | number | yes |  |
| `params.params.name` | string | yes |  |
| `params.params.projectId` | number | yes |  |
| `params.params.startDate` | string | yes |  |
| `params.params.endDate` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sprint.md) for the provider-specific parameters and requirements.

