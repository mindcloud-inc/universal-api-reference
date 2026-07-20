# JigsawStack: Extract Text with vOCR



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/extract-text-with-vocr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/extract-text-with-vocr?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/extract-text-with-vocr?${params}`, {
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
      "context": {},
      "has_text": true,
      "height": 1,
      "sections": [
        {}
      ],
      "success": true,
      "tags": [
        "string"
      ],
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_usage` | object |  |
| `context` | object |  |
| `has_text` | boolean |  |
| `height` | number |  |
| `sections` | array<object> |  |
| `success` | boolean |  |
| `tags` | array<string> |  |
| `width` | number |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/vocr` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-text-with-vocr.md) for the provider-specific parameters and requirements.

