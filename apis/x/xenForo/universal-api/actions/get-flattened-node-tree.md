# XenForo: Get Flattened Node Tree

Retrieves the flattened node tree from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-flattened-node-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-flattened-node-tree?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-flattened-node-tree?${params}`, {
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
      "nodes_flat": [
        {
          "depth": 1,
          "node": {
            "node_id": 1,
            "node_type_id": "string",
            "title": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nodes_flat` | array<object> |  |
| `nodes_flat[].depth` | number |  |
| `nodes_flat[].node.node_id` | number |  |
| `nodes_flat[].node.node_type_id` | string |  |
| `nodes_flat[].node.title` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /nodes/flattened` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flattened-node-tree.md) for the provider-specific parameters and requirements.

