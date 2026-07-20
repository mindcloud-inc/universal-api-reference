# Piloterr: Search Google News



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google-news?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google-news?${params}`, {
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
| `query` | string | yes | Google News search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "news": {
        "link": "https://example.com",
        "source": "string",
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
| `news.link` | string |  |
| `news.source` | string |  |
| `news.title` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /google/news` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-news.md) for the provider-specific parameters and requirements.

