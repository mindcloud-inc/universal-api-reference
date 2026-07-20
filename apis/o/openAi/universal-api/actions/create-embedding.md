# Open AI: Create Embedding

Creates text embeddings in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-embedding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-embedding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "text-embedding-3-small",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-embedding', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "text-embedding-3-small",
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | list | yes | Embedding model ID. Default: `text-embedding-3-small`. |
| `input` | string | yes | Input text or token array to embed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "embedding": [
            1
          ],
          "index": 1,
          "object": "string"
        }
      ],
      "model": "string",
      "object": "string",
      "usage": {
        "promptTokens": 1,
        "totalTokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].embedding[]` | number |  |
| `data[].index` | number |  |
| `data[].object` | string |  |
| `model` | string |  |
| `object` | string |  |
| `usage.promptTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/embeddings` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embedding.md) for the provider-specific parameters and requirements.

