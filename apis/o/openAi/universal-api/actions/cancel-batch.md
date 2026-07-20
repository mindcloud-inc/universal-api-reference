# Open AI: Cancel Batch

Cancels a batch in Open AI.

```
PUT https://connect.mindcloud.co/v1/universal/openAi/latest/actions/cancel-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batch_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/cancel-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batch_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch_id` | string | yes | The ID of the batch to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelledAt": "2026-05-07T12:00:00.000Z",
      "cancellingAt": "2026-05-07T12:00:00.000Z",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "completionWindow": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endpoint": "string",
      "errorFileId": {},
      "errors": {},
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "failedAt": "2026-05-07T12:00:00.000Z",
      "finalizingAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inProgressAt": "2026-05-07T12:00:00.000Z",
      "inputFileId": "string",
      "metadata": {},
      "model": {},
      "object": "string",
      "outputFileId": {},
      "requestCounts": {
        "completed": 1,
        "failed": 1,
        "total": 1
      },
      "status": "string",
      "usage": {
        "inputTokens": 1,
        "inputTokensDetails": {
          "cachedTokens": 1
        },
        "outputTokens": 1,
        "outputTokensDetails": {
          "reasoningTokens": 1
        },
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
| `cancelledAt` | date |  |
| `cancellingAt` | date |  |
| `completedAt` | date |  |
| `completionWindow` | string |  |
| `createdAt` | date |  |
| `endpoint` | string |  |
| `errorFileId` | object |  |
| `errors` | object |  |
| `expiredAt` | date |  |
| `expiresAt` | date |  |
| `failedAt` | date |  |
| `finalizingAt` | date |  |
| `id` | string |  |
| `inProgressAt` | date |  |
| `inputFileId` | string |  |
| `metadata` | object |  |
| `model` | object |  |
| `object` | string |  |
| `outputFileId` | object |  |
| `requestCounts.completed` | number |  |
| `requestCounts.failed` | number |  |
| `requestCounts.total` | number |  |
| `status` | string |  |
| `usage.inputTokens` | number |  |
| `usage.inputTokensDetails.cachedTokens` | number |  |
| `usage.outputTokens` | number |  |
| `usage.outputTokensDetails.reasoningTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/batches/:batch_id/cancel` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-batch.md) for the provider-specific parameters and requirements.

