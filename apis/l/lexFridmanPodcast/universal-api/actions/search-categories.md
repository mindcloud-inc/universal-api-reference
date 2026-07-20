# Lex Fridman Podcast: Search Categories

Finds categories in Lex Fridman Podcast by search term.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-categories?connectionId=$CONNECTION_ID&limit=25&offset=0&search=ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "ai"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-categories?${params}`, {
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
| `search` | string | yes | The category search query. Default: `ai`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "parent": 1,
      "slug": "string",
      "taxonomy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `description` | string |  |
| `id` | number |  |
| `link` | string |  |
| `name` | string |  |
| `parent` | number |  |
| `slug` | string |  |
| `taxonomy` | string |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/wp/v2/categories` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-categories.md) for the provider-specific parameters and requirements.

