# JigsawStack: Transcribe Audio



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/transcribe-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/transcribe-audio?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/transcribe-audio?${params}`, {
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
      "chunks": [
        {}
      ],
      "log_id": "string",
      "speakers": [
        {}
      ],
      "success": true,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_usage` | object |  |
| `chunks` | array<object> |  |
| `log_id` | string |  |
| `speakers` | array<object> |  |
| `success` | boolean |  |
| `text` | string |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/ai/transcribe` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transcribe-audio.md) for the provider-specific parameters and requirements.

