# Piloterr: Search Google Videos



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google-videos?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google-videos?${params}`, {
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
| `gl` | string | no | Two-letter Google country code. |
| `hl` | string | no | Two-letter Google language code. |
| `page` | string | no | Results page number. |
| `query` | string | yes | Google Videos search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "videos": {
        "channel": "string",
        "link": "https://example.com",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `videos.channel` | string |  |
| `videos.link` | string |  |
| `videos.title` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /google/videos` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-videos.md) for the provider-specific parameters and requirements.

