# Anthropic: Create Message Batch

Creates a new message batch in Anthropic.

```
POST https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-message-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-message-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-message-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requests[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requests[]` | array<object> | yes | List of requests to process in the batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "string",
      "cancelInitiatedAt": "string",
      "createdAt": "string",
      "endedAt": "string",
      "expiresAt": "string",
      "id": "string",
      "processingStatus": "string",
      "requestCounts": {},
      "resultsUrl": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | string |  |
| `cancelInitiatedAt` | string |  |
| `createdAt` | string |  |
| `endedAt` | string |  |
| `expiresAt` | string |  |
| `id` | string |  |
| `processingStatus` | string |  |
| `requestCounts` | object |  |
| `resultsUrl` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Anthropic API, this operation is `POST /v1/messages/batches` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message-batch.md) for the provider-specific parameters and requirements.

