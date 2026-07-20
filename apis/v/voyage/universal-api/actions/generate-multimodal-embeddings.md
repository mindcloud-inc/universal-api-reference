# Voyage: Generate Multimodal Embeddings

Generates multimodal embeddings in Voyage.

```
POST https://connect.mindcloud.co/v1/universal/voyage/latest/actions/generate-multimodal-embeddings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/generate-multimodal-embeddings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputs[]": [
    {}
  ],
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voyage/latest/actions/generate-multimodal-embeddings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputs[]": [{}],
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputs[]` | array<object> | yes | Multimodal inputs to embed. |
| `model` | string | yes | Multimodal embedding model to use. |
| `inputType` | list | no | Optional input type for retrieval-aware embeddings. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "embedding": [
        1
      ],
      "index": 1,
      "object": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embedding` | array<number> |  |
| `index` | number |  |
| `object` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Voyage API, this operation is `POST /v1/multimodalembeddings` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-multimodal-embeddings.md) for the provider-specific parameters and requirements.

