# Leantime: Update Milestone



```
PUT https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-milestone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.params.id": 1,
  "params.params.headline": "string",
  "params.params.status": "3",
  "params.params.editorId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-milestone', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.params.id": 1,
    "params.params.headline": "string",
    "params.params.status": "3",
    "params.params.editorId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.params.id` | number | yes |  |
| `params.params.headline` | string | yes |  |
| `params.params.status` | number | yes | Default: `3`. |
| `params.params.editorId` | number | yes |  |
| `params.params.dependentMilestone` | string | no |  |
| `params.params.tags` | string | no |  |
| `params.params.editFrom` | string | no |  |
| `params.params.editTo` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-milestone.md) for the provider-specific parameters and requirements.

