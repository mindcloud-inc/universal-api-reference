# Groq: Create Embedding

Creates an embedding in Groq.

```
POST https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-embedding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-embedding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-embedding', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | The Groq embedding model identifier to use. |
| `input` | string | yes | Text input to embed. Groq also supports array input, which is not yet fully modeled in this scaffold. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `encodingFormat` | list | no | Embedding output format. |
| `user` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Groq API returns.

## Native endpoint

Through the native Groq API, this operation is `POST /openai/v1/embeddings` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embedding.md) for the provider-specific parameters and requirements.

