# Voyage: Generate Contextualized Embeddings

Generates contextualized chunk embeddings in Voyage.

```
POST https://connect.mindcloud.co/v1/universal/voyage/latest/actions/generate-contextualized-embeddings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/generate-contextualized-embeddings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputs[]": [
    [
      "string"
    ]
  ],
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voyage/latest/actions/generate-contextualized-embeddings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputs[]": [["string"]],
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputs[]` | array<array> | yes | Nested input lists to embed with context. |
| `model` | string | yes | Contextualized embedding model to use. |
| `inputType` | list | no | Optional input type for retrieval-aware embeddings. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "index": 1,
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `index` | number |  |
| `object` | string |  |

## Native endpoint

Through the native Voyage API, this operation is `POST /v1/contextualizedembeddings` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-contextualized-embeddings.md) for the provider-specific parameters and requirements.

