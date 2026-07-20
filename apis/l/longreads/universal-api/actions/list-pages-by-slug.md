# Longreads: List Pages By Slug

Finds Longreads pages by page slug.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-pages-by-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-pages-by-slug?connectionId=$CONNECTION_ID&limit=25&offset=0&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-pages-by-slug?${params}`, {
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
| `slug` | string | yes | The page slug to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "featured_media": 1,
      "id": 1,
      "link": "https://example.com",
      "menu_order": 1,
      "parent": 1,
      "slug": "string",
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
| `date` | date |  |
| `featured_media` | number |  |
| `id` | number |  |
| `link` | string |  |
| `menu_order` | number |  |
| `parent` | number |  |
| `slug` | string |  |
| `title` | object |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/pages` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pages-by-slug.md) for the provider-specific parameters and requirements.

