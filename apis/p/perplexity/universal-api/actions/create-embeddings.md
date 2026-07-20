# Perplexity: Create Embeddings

Creates embeddings from text in Perplexity.

```
POST https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-embeddings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-embeddings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string",
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-embeddings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string",
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Input text to embed. Perplexity also accepts arrays of strings; this action currently models the common single-input path. |
| `model` | string | yes | Embedding model to use. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dimensions` | number | no | Optional output embedding dimensions. |
| `encodingFormat` | string | no | Output encoding format, for example base64_int8 or base64_binary. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "embedding": "string",
          "index": 1,
          "object": "string"
        }
      ],
      "model": "string",
      "object": "string",
      "usage": {
        "prompt_tokens": 1,
        "total_tokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].embedding` | string |  |
| `data[].index` | number |  |
| `data[].object` | string |  |
| `model` | string |  |
| `object` | string |  |
| `usage.prompt_tokens` | number |  |
| `usage.total_tokens` | number |  |

## Native endpoint

Through the native Perplexity API, this operation is `POST /v1/embeddings` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embeddings.md) for the provider-specific parameters and requirements.

