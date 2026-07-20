# Pexels: List Popular Videos

Retrieves popular video results from Pexels.

```
GET https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-popular-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pexels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-popular-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-popular-videos?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minWidth` | number | no | Minimum width in pixels of returned videos. |
| `minHeight` | number | no | Minimum height in pixels of returned videos. |
| `minDuration` | number | no | Minimum duration in seconds of returned videos. |
| `maxDuration` | number | no | Maximum duration in seconds of returned videos. |

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
| `url` | string | Pexels URL for popular videos. |
| `videos` | array<object> | Popular video results returned by Pexels. |

## Native endpoint

Through the native Pexels API, this operation is `GET /v1/videos/popular` (base URL `https://api.pexels.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-popular-videos.md) for the provider-specific parameters and requirements.

