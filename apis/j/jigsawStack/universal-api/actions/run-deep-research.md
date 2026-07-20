# JigsawStack: Run Deep Research



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/run-deep-research
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/run-deep-research?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/run-deep-research?${params}`, {
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
      "_usage": {},
      "geo_results": [
        {}
      ],
      "image_urls": [
        "https://example.com"
      ],
      "links": [
        "https://example.com"
      ],
      "log_id": "string",
      "query": "string",
      "results": "string",
      "sources": [
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
| `_usage` | object |  |
| `geo_results` | array<object> |  |
| `image_urls` | array<string> |  |
| `links` | array<string> |  |
| `log_id` | string |  |
| `query` | string |  |
| `results` | string |  |
| `sources` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/web/deep_research` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-deep-research.md) for the provider-specific parameters and requirements.

