# Perplexity: Create Contextualized Embeddings

Creates contextualized embeddings from text in Perplexity.

```
POST https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-contextualized-embeddings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-contextualized-embeddings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input[]": [
    [
      "string"
    ]
  ],
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-contextualized-embeddings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input[]": [["string"]],
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input[]` | array<array> | yes | Nested array of document chunks. Each inner array represents one document. |
| `model` | string | yes | Contextualized embedding model to use. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dimensions` | number | no | Optional output embedding dimensions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "data": [
            {
              "embedding": "string",
              "index": 1,
              "object": "string"
            }
          ],
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
| `data[].data[].embedding` | string |  |
| `data[].data[].index` | number |  |
| `data[].data[].object` | string |  |
| `data[].index` | number |  |
| `data[].object` | string |  |
| `model` | string |  |
| `object` | string |  |
| `usage.prompt_tokens` | number |  |
| `usage.total_tokens` | number |  |

## Native endpoint

Through the native Perplexity API, this operation is `POST /v1/contextualizedembeddings` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contextualized-embeddings.md) for the provider-specific parameters and requirements.

