# Pinecone: Generate Vectors

Generates vectors from input data in Pinecone.

```
POST https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/generate-vectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/generate-vectors" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "multilingual-e5-large",
  "inputs[].text": "The quick brown fox jumps over the lazy dog.",
  "parameters.inputType": "passage"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/generate-vectors', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "multilingual-e5-large",
    "inputs[].text": "The quick brown fox jumps over the lazy dog.",
    "parameters.inputType": "passage"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | The embedding model to use. Example: `multilingual-e5-large`. |
| `inputs[].text` | string | yes | The text input to generate an embedding for. Example: `The quick brown fox jumps over the lazy dog.`. |
| `parameters.inputType` | string | yes | The input type required by the model: query or passage. Example: `passage`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters.truncate` | string | no | Optional truncation behavior for overlong inputs. Example: `END`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "sparse_indices": [
            1
          ],
          "sparse_tokens": [
            "string"
          ],
          "sparse_values": [
            1
          ],
          "values": [
            1
          ],
          "vector_type": "string"
        }
      ],
      "model": "string",
      "usage": {
        "total_tokens": 1
      },
      "vector_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].sparse_indices[]` | number |  |
| `data[].sparse_tokens[]` | string |  |
| `data[].sparse_values[]` | number |  |
| `data[].values[]` | number |  |
| `data[].vector_type` | string |  |
| `model` | string |  |
| `usage.total_tokens` | number |  |
| `vector_type` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `POST /embed` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-vectors.md) for the provider-specific parameters and requirements.

