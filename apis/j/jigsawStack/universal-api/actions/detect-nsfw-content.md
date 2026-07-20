# JigsawStack: Detect NSFW Content



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-nsfw-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-nsfw-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-nsfw-content?${params}`, {
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
      "gore": true,
      "gore_score": 1,
      "log_id": "string",
      "nsfw": true,
      "nsfw_score": 1,
      "nudity": true,
      "nudity_score": 1,
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
| `gore` | boolean |  |
| `gore_score` | number |  |
| `log_id` | string |  |
| `nsfw` | boolean |  |
| `nsfw_score` | number |  |
| `nudity` | boolean |  |
| `nudity_score` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/validate/nsfw` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-nsfw-content.md) for the provider-specific parameters and requirements.

