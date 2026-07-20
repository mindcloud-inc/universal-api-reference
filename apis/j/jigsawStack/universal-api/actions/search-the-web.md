# JigsawStack: Search the Web



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/search-the-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/search-the-web?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/search-the-web?${params}`, {
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
      "ai_overview": "string",
      "geo_results": [
        {}
      ],
      "image_urls": [
        "https://example.com"
      ],
      "is_safe": true,
      "query": "string",
      "results": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_overview` | string |  |
| `geo_results` | array<object> |  |
| `image_urls` | array<string> |  |
| `is_safe` | boolean |  |
| `query` | string |  |
| `results` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/web/search` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-the-web.md) for the provider-specific parameters and requirements.

