# Longreads: Search Media

Finds Longreads media items by search text.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/search-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/search-media?connectionId=$CONNECTION_ID&limit=25&offset=0&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/search-media?${params}`, {
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
| `search` | string | yes | Text to search in media items. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link": "https://example.com",
      "media_type": "string",
      "mime_type": "string",
      "slug": "string",
      "source_url": "https://example.com",
      "title": {},
      "type": "string"
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
| `id` | number |  |
| `link` | string |  |
| `media_type` | string |  |
| `mime_type` | string |  |
| `slug` | string |  |
| `source_url` | string |  |
| `title` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/media` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-media.md) for the provider-specific parameters and requirements.

