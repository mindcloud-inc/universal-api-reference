# Notion: List Comments

Retrieves comments from the connected Notion workspace.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&blockId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "blockId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-comments?${params}`, {
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
| `blockId` | string | yes | ID of the page or block to list comments for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startCursor` | string | no | Cursor for pagination. |
| `pageSize` | number | no | Maximum number of comments per page (max 100). Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "nextCursor": "string",
      "object": "string",
      "results": [
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
| `hasMore` | boolean | Whether more comments are available. |
| `nextCursor` | string | Cursor for next page. |
| `object` | string | List wrapper type. |
| `results` | array<object> | Comment results. |

## Native endpoint

Through the native Notion API, this operation is `GET /comments` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

