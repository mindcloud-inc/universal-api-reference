# Leantime: Create Milestone



```
POST https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-milestone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.params.headline": "string",
  "params.params.projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/create-milestone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.params.headline": "string",
    "params.params.projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.params.headline` | string | yes | The milestone headline. |
| `params.params.projectId` | number | yes | The project that will own the milestone. |
| `params.params.editFrom` | string | no | Optional start date in user format or ISO8601. |
| `params.params.editTo` | string | no | Optional end date in user format or ISO8601. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.params.dependentMilestone` | number | no | Optional parent milestone ID. |
| `params.params.tags` | string | no | Optional milestone tags. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-milestone.md) for the provider-specific parameters and requirements.

