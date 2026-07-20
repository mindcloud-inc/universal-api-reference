# JigsawStack: Generate Image



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/generate-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/generate-image?${params}`, {
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
      "success": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_usage` | object |  |
| `success` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/ai/image_generation` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

