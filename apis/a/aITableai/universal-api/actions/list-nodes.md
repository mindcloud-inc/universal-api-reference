# AITable.ai: List Nodes

Retrieves nodes from a space in AITable.ai.

```
GET https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-nodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-nodes?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-nodes?${params}`, {
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
| `nodeType` | string | no | Optional node type filter when listing nodes. |
| `spaceId` | string | yes | AITable space ID whose root nodes should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nodes": [
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
| `nodes` | array<object> | Nodes in the selected space. |

## Native endpoint

Through the native AITable.ai API, this operation is `GET /fusion/v1/spaces/:spaceId/nodes` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nodes.md) for the provider-specific parameters and requirements.

