# Workflowy: List Nodes

Retrieves child nodes from Workflowy for a parent.

```
GET https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/list-nodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workflowy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/list-nodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/list-nodes?${params}`, {
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
| `parentId` | string | no | Node UUID, target key like home or inbox, or None for top-level nodes. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean | Whether the node is completed. |
| `completedAt` | number | Unix timestamp when the node was completed, when applicable. |
| `createdAt` | number | Unix timestamp when the node was created. |
| `data.layoutMode` | string | The node layout mode. |
| `id` | string | The unique identifier of the node. |
| `modifiedAt` | number | Unix timestamp when the node was last modified. |
| `name` | string | The node title. |
| `note` | string | The note content attached to the node, when present. |
| `parentId` | string | The identifier of the parent node or target. |
| `priority` | number | The Workflowy display priority for the node. |

## Native endpoint

Through the native Workflowy API, this operation is `GET /nodes` (base URL `https://workflowy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nodes.md) for the provider-specific parameters and requirements.

