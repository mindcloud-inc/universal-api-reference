# World News API: Extract News Links

Extracts news article links from a website using World News API.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/extract-news-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/extract-news-links?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.cnn.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.cnn.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/extract-news-links?${params}`, {
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
| `analyze` | boolean | no | When true, analyze extracted links in more detail. |
| `url` | string | yes | Website or article URL to extract news links from. Default: `https://www.cnn.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "news_links": [
        "https://example.com"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `news_links` | array<string> | Extracted news article links. |
| `status` | string | Extraction status. |

## Native endpoint

Through the native World News API API, this operation is `GET /extract-news-links` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-news-links.md) for the provider-specific parameters and requirements.

