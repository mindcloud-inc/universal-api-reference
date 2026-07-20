# CometAPI: Create Embedding

Creates embeddings in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/create-embedding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/create-embedding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string",
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/create-embedding', {
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
| `input` | string | yes | Text or tokens to embed. |
| `model` | string | yes | Embedding model ID. |

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
      "object": "string",
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
| `object` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /v1/embeddings` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embedding.md) for the provider-specific parameters and requirements.

