# Freepik: Search Music

Finds Freepik music by search term and filters.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-music
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-music?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-music?${params}`, {
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
| `q` | string | no | Music search query. Default: `happy`. |
| `limit` | number | no | Maximum number of music tracks to return. Default: `1`. |
| `offset` | number | no | Zero-based music result offset. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "results": [
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
| `count` | number | Total matching music tracks. |
| `results` | array<object> | Matching music tracks. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/music` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-music.md) for the provider-specific parameters and requirements.

