# Lex Fridman Podcast: Search Pages

Finds pages in Lex Fridman Podcast by search term.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&search=app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "app"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-pages?${params}`, {
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
| `search` | string | yes | The page search query. Default: `app`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": 1,
      "content": {},
      "date": "2026-05-07T12:00:00.000Z",
      "dateGmt": "2026-05-07T12:00:00.000Z",
      "excerpt": {},
      "featuredMedia": 1,
      "id": 1,
      "link": "https://example.com",
      "modified": "2026-05-07T12:00:00.000Z",
      "modifiedGmt": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
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
| `content` | object |  |
| `date` | date |  |
| `dateGmt` | date |  |
| `excerpt` | object |  |
| `featuredMedia` | number |  |
| `id` | number |  |
| `link` | string |  |
| `modified` | date |  |
| `modifiedGmt` | date |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/wp/v2/pages` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-pages.md) for the provider-specific parameters and requirements.

