# Lex Fridman Podcast: Search Content

Finds content in Lex Fridman Podcast by search term.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-content?connectionId=$CONNECTION_ID&limit=25&offset=0&search=Lex" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "Lex"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/search-content?${params}`, {
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
| `search` | string | yes | The site content search query. Default: `Lex`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "subtype": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `subtype` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/wp/v2/search` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-content.md) for the provider-specific parameters and requirements.

