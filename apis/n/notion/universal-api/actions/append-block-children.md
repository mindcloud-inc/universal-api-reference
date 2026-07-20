# Notion: Append Block Children

Appends child blocks to a Notion block.

```
PUT https://connect.mindcloud.co/v1/universal/notion/latest/actions/append-block-children
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/append-block-children" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blockId": "string",
  "children": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/append-block-children', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blockId": "string",
    "children": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blockId` | string | yes | ID of the parent block where children are appended. |
| `children` | list<object> | yes | Array of block objects to append as children. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `position` | object | no | Optional insertion position object for append operations. |
| `after` | string | no | Deprecated: ID of existing child block to append after. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block": {},
      "hasMore": true,
      "nextCursor": "string",
      "object": "string",
      "requestId": "string",
      "results": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block` | object |  |
| `hasMore` | boolean |  |
| `nextCursor` | string |  |
| `object` | string |  |
| `requestId` | string |  |
| `results` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Notion API, this operation is `PATCH /blocks/:block_id/children` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/append-block-children.md) for the provider-specific parameters and requirements.

