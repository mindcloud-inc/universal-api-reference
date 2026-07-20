# XenForo: Get Node

Retrieves the specified node from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-node?connectionId=$CONNECTION_ID&id=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-node?${params}`, {
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
| `id` | number | yes | ID of the node to retrieve. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "node": {
        "node_id": 1,
        "node_type_id": "string",
        "parent_node_id": 1,
        "title": "string",
        "view_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `node.node_id` | number |  |
| `node.node_type_id` | string |  |
| `node.parent_node_id` | number |  |
| `node.title` | string |  |
| `node.view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /nodes/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-node.md) for the provider-specific parameters and requirements.

