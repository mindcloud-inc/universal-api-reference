# Typesense: Create Embeddings

Creates new vector embeddings in Typesense.

```
POST https://connect.mindcloud.co/v1/universal/typesense/latest/actions/create-embeddings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/create-embeddings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "embeddingRequest": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typesense/latest/actions/create-embeddings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "embeddingRequest": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `embeddingRequest` | object | yes | OpenAI-compatible embedding request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "model": "string",
      "response": {},
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `model` | string |  |
| `response` | object |  |
| `usage` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `POST /v1/embeddings` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embeddings.md) for the provider-specific parameters and requirements.

