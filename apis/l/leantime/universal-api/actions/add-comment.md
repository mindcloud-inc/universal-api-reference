# Leantime: Add Comment



```
POST https://connect.mindcloud.co/v1/universal/leantime/latest/actions/add-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.module": "project",
  "entityId": 1,
  "params.values.text": "string",
  "params.values.father": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.module": "project",
    "entityId": 1,
    "params.values.text": "string",
    "params.values.father": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.module` | string | yes | The Leantime module name. Default: `project`. |
| `entityId` | number | yes | The target entity id. |
| `params.values.text` | string | yes | Comment text. |
| `params.values.father` | number | yes | Parent comment id; use 0 for a new top-level comment. Default: `0`. |
| `params.values.status` | string | no | Optional comment status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment.md) for the provider-specific parameters and requirements.

