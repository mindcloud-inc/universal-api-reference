# Groq: Cancel Batch

Cancels a batch in Groq.

```
PUT https://connect.mindcloud.co/v1/universal/groq/latest/actions/cancel-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/groq/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/cancel-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelledAt": 1,
      "cancellingAt": 1,
      "completedAt": 1,
      "completionWindow": "string",
      "createdAt": 1,
      "endpoint": "string",
      "errorFileId": "string",
      "errors": {},
      "expiredAt": 1,
      "expiresAt": 1,
      "failedAt": 1,
      "finalizingAt": 1,
      "id": "string",
      "inProgressAt": 1,
      "inputFileId": "string",
      "metadata": {},
      "object": "string",
      "outputFileId": "string",
      "requestCounts": {
        "completed": 1,
        "failed": 1,
        "total": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelledAt` | number |  |
| `cancellingAt` | number |  |
| `completedAt` | number |  |
| `completionWindow` | string |  |
| `createdAt` | number |  |
| `endpoint` | string |  |
| `errorFileId` | string |  |
| `errors` | object |  |
| `expiredAt` | number |  |
| `expiresAt` | number |  |
| `failedAt` | number |  |
| `finalizingAt` | number |  |
| `id` | string |  |
| `inProgressAt` | number |  |
| `inputFileId` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `outputFileId` | string |  |
| `requestCounts.completed` | number |  |
| `requestCounts.failed` | number |  |
| `requestCounts.total` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Groq API, this operation is `POST /openai/v1/batches/:batch_id/cancel` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-batch.md) for the provider-specific parameters and requirements.

