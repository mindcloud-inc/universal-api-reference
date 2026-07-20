# Dynalist: Insert Node

Creates a new document node in Dynalist.

```
POST https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/insert-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/insert-node" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "parentId": "string",
  "index": "-1",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/insert-node', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "parentId": "string",
    "index": "-1",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | ID of the document to edit. |
| `parentId` | string | yes | ID of the parent node. |
| `index` | number | yes | Zero-indexed destination position; use -1 for the end. Default: `-1`. |
| `content` | string | yes | Node content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | no | Optional node note. |
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

Through the native Dynalist API, this operation is `POST /doc/edit` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-node.md) for the provider-specific parameters and requirements.

