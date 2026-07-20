# Pexels: Search Videos

Finds videos in Pexels by search query.

```
GET https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pexels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-videos?${params}`, {
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
| `query` | string | yes | Topic to search for, such as Ocean, Tigers, or Group of people working. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orientation` | string | no | Desired video orientation: landscape, portrait, or square. |
| `size` | string | no | Minimum video size: large, medium, or small. |
| `locale` | string | no | Locale for the search, such as en-US, pt-BR, or es-ES. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_page": "string",
      "page": 1,
      "per_page": 1,
      "prev_page": "string",
      "total_results": 1,
      "url": "https://example.com",
      "videos": [
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
| `next_page` | string | Next page URL when available. |
| `page` | number | Current page number. |
| `per_page` | number | Number of results returned per page. |
| `prev_page` | string | Previous page URL when available. |
| `total_results` | number | Total number of matching results. |
| `url` | string | Pexels URL for the current search query. |
| `videos` | array<object> | Video results returned by Pexels. |

## Native endpoint

Through the native Pexels API, this operation is `GET /v1/videos/search` (base URL `https://api.pexels.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-videos.md) for the provider-specific parameters and requirements.

