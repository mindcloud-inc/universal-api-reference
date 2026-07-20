# Longreads: List Posts Published After Date

Retrieves Longreads posts published after a date.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-posts-published-after-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-posts-published-after-date?connectionId=$CONNECTION_ID&limit=25&offset=0&after=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "after": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-posts-published-after-date?${params}`, {
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
| `after` | date | yes | Return posts published after this ISO 8601 datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": 1,
      "categories": [
        1
      ],
      "date": "2026-05-07T12:00:00.000Z",
      "featured_media": 1,
      "id": 1,
      "link": "https://example.com",
      "slug": "string",
      "tags": [
        1
      ],
      "title": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | number |  |
| `categories` | array<number> |  |
| `date` | date |  |
| `featured_media` | number |  |
| `id` | number |  |
| `link` | string |  |
| `slug` | string |  |
| `tags` | array<number> |  |
| `title` | object |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/posts` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts-published-after-date.md) for the provider-specific parameters and requirements.

