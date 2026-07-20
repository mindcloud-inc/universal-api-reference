# Fliz: List videos

Retrieves videos from your Fliz account.

```
GET https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliz `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-videos?${params}`, {
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
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": {},
      "format": "string",
      "id": "string",
      "lang": "string",
      "step": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Video category. |
| `createdAt` | date | Creation timestamp. |
| `error` | object | Provider error payload when generation fails. |
| `format` | string | Video output format. |
| `id` | string | Video UUID. |
| `lang` | string | Video language code. |
| `step` | string | Current processing step. |
| `title` | string | Video title. |
| `url` | string | Rendered video URL when available. |

## Native endpoint

Through the native Fliz API, this operation is `GET /api/rest/videos` (base URL `https://app.fliz.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.

