# Longreads: List Comments

Retrieves comments from the Longreads site.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-comments?${params}`, {
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
      "author_name": "Ava Chen",
      "content": {},
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link": "https://example.com",
      "parent": 1,
      "post": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_name` | string |  |
| `content` | object |  |
| `date` | date |  |
| `id` | number |  |
| `link` | string |  |
| `parent` | number |  |
| `post` | number |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/comments` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

