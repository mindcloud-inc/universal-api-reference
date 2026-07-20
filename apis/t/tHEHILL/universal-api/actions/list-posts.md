# THE HILL: List Posts

Retrieves published posts from The Hill.

```
GET https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a THE HILL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/list-posts?${params}`, {
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
| `order` | string | no | Sort direction for the post list. Default: `desc`. |
| `orderby` | string | no | Sort posts by a WordPress field. Default: `date`. |
| `page` | number | no | Page number to fetch. Default: `1`. |
| `perPage` | number | no | Number of posts to return per page. Default: `20`. |
| `search` | string | no | Search posts by keyword. |
| `slug` | string | no | Filter posts by slug. |

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
      "excerpt": {
        "rendered": "string"
      },
      "featured_media": 1,
      "id": 1,
      "link": "https://example.com",
      "modified": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
      "tags": [
        1
      ],
      "title": {
        "rendered": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | number | Author ID |
| `categories` | array<number> | Category IDs |
| `date` | date | Post publish date |
| `excerpt.rendered` | string | Rendered post excerpt |
| `featured_media` | number | Featured media ID |
| `id` | number | WordPress post ID |
| `link` | string | Canonical post URL |
| `modified` | date | Last modified timestamp |
| `slug` | string | Post slug |
| `status` | string | Post status |
| `tags` | array<number> | Tag IDs |
| `title.rendered` | string | Rendered post title |
| `type` | string | Post type |

## Native endpoint

Through the native THE HILL API, this operation is `GET /wp/v2/posts` (base URL `https://thehill.com/wp-json/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

