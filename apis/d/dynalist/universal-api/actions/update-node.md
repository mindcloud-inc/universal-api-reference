# Dynalist: Update Node

Updates a document node in Dynalist.

```
PUT https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/update-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/update-node" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "nodeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/update-node', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "nodeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | ID of the document to edit. |
| `nodeId` | string | yes | ID of the node to update. |
| `content` | string | no | New node content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | no | New node note. |
| `checked` | boolean | no | Whether the node is checked. |
| `checkbox` | boolean | no | Whether the node has a checkbox. |
| `heading` | number | no | Heading level. |
| `color` | number | no | Dynalist color index. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_code": "string",
      "_msg": "string",
      "new_node_ids": [
        "string"
      ],
      "results": [
        true
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_code` | string |  |
| `_msg` | string |  |
| `new_node_ids` | array<string> |  |
| `results` | array<boolean> |  |

## Native endpoint

Through the native Dynalist API, this operation is `POST /doc/edit` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-node.md) for the provider-specific parameters and requirements.

