# Workflowy: Export All Nodes

Retrieves all Workflowy nodes as a flat list.

```
GET https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/export-all-nodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workflowy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/export-all-nodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/export-all-nodes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Workflowy API, this operation is `GET /nodes-export` (base URL `https://workflowy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-all-nodes.md) for the provider-specific parameters and requirements.

