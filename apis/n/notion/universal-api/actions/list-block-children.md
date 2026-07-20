# Notion: List Block Children

Retrieves child blocks for a Notion block.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-block-children
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-block-children?connectionId=$CONNECTION_ID&limit=25&offset=0&blockId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "blockId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-block-children?${params}`, {
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
| `blockId` | string | yes | ID of the parent block. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Maximum number of children to return (max 100). |
| `startCursor` | string | no | Cursor from a previous response to continue pagination. |

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

Through the native Notion API, this operation is `GET /blocks/:block_id/children` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-block-children.md) for the provider-specific parameters and requirements.

