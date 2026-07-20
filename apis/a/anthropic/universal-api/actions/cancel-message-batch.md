# Anthropic: Cancel Message Batch

Cancels a message batch in Anthropic.

```
PUT https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/cancel-message-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/cancel-message-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageBatchId": "msgbatch_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/cancel-message-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageBatchId": "msgbatch_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageBatchId` | string | yes | The Message Batch ID. Example: `msgbatch_123`. |

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

Through the native Anthropic API, this operation is `POST /v1/messages/batches/:message_batch_id/cancel` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-message-batch.md) for the provider-specific parameters and requirements.

