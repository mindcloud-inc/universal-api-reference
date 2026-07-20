# XenForo: Get Node Tree

Retrieves the node tree from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-node-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-node-tree?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-node-tree?${params}`, {
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
      "nodes": [
        {
          "node_id": 1,
          "node_type_id": "string",
          "parent_node_id": 1,
          "title": "string",
          "view_url": "https://example.com"
        }
      ],
      "tree_map": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nodes` | array<object> |  |
| `nodes[].node_id` | number |  |
| `nodes[].node_type_id` | string |  |
| `nodes[].parent_node_id` | number |  |
| `nodes[].title` | string |  |
| `nodes[].view_url` | string |  |
| `tree_map` | array<object> |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /nodes/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-node-tree.md) for the provider-specific parameters and requirements.

