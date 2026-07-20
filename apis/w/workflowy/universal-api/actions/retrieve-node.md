# Workflowy: Retrieve Node

Retrieves a Workflowy node by target or ID.

```
GET https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/retrieve-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workflowy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/retrieve-node?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/retrieve-node?${params}`, {
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
| `id` | string | yes | The identifier of the node to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "node": {
        "completed": true,
        "completedAt": 1,
        "createdAt": 1,
        "data": {
          "layoutMode": "string"
        },
        "id": "string",
        "modifiedAt": 1,
        "name": "Ava Chen",
        "note": "string",
        "parentId": "string",
        "priority": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `node.completed` | boolean | Whether the node is completed. |
| `node.completedAt` | number | Unix timestamp when the node was completed, when applicable. |
| `node.createdAt` | number | Unix timestamp when the node was created. |
| `node.data.layoutMode` | string | The node layout mode. |
| `node.id` | string | The unique identifier of the node. |
| `node.modifiedAt` | number | Unix timestamp when the node was last modified. |
| `node.name` | string | The node title. |
| `node.note` | string | The note content attached to the node, when present. |
| `node.parentId` | string | The identifier of the parent node or target. |
| `node.priority` | number | The Workflowy display priority for the node. |

## Native endpoint

Through the native Workflowy API, this operation is `GET /nodes/:id` (base URL `https://workflowy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-node.md) for the provider-specific parameters and requirements.

