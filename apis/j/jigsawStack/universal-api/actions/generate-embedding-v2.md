# JigsawStack: Generate Embedding v2



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/generate-embedding-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/generate-embedding-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/generate-embedding-v2?${params}`, {
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
        "string"
      ],
      "embeddings": [
        [
          "string"
        ]
      ],
      "log_id": "string",
      "speaker_embeddings": [
        [
          "string"
        ]
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
| `chunks` | array<string> |  |
| `embeddings` | array<array> |  |
| `log_id` | string |  |
| `speaker_embeddings` | array<array> |  |
| `success` | boolean |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v2/embedding` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-embedding-v2.md) for the provider-specific parameters and requirements.

