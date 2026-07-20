# Cohere: Embed

Generates embeddings for text or images in Cohere.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/embed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/embed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/embed?${params}`, {
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
      "embeddings": {},
      "id": "string",
      "images": [
        {}
      ],
      "meta": {},
      "responseType": "string",
      "texts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embeddings` | object |  |
| `id` | string |  |
| `images` | array<object> |  |
| `meta` | object |  |
| `responseType` | string |  |
| `texts` | array<object> |  |

## Native endpoint

Through the native Cohere API, this operation is `POST /v1/embed` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/embed.md) for the provider-specific parameters and requirements.

