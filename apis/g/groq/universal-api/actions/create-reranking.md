# Groq: Create Reranking

Creates a reranking result in Groq.

```
POST https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-reranking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-reranking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "query": "string",
  "docs[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-reranking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "query": "string",
    "docs[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes |  |
| `query` | string | yes |  |
| `docs[]` | array<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instruction` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Groq API returns.

## Native endpoint

Through the native Groq API, this operation is `POST /openai/v1/reranking` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reranking.md) for the provider-specific parameters and requirements.

