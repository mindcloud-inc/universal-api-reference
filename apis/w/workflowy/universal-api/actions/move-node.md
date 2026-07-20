# Workflowy: Move Node

Moves a node to a new parent in Workflowy.

```
PUT https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/move-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workflowy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/move-node" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/move-node', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The identifier of the node to move. |
| `parentId` | string | no | The new parent node identifier or target key. |
| `position` | string | no | Where to place the moved node: top or bottom. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Workflowy operation status. |

## Native endpoint

Through the native Workflowy API, this operation is `POST /nodes/:id/move` (base URL `https://workflowy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-node.md) for the provider-specific parameters and requirements.

