# Open AI: Retrieve Batch

Retrieves a batch from Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/retrieve-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/retrieve-batch?connectionId=$CONNECTION_ID&batch_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batch_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/retrieve-batch?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch_id` | string | yes | The ID of the batch to retrieve. |

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
      "errors": {
        "data": [
          {
            "code": "string",
            "line": {},
            "message": "string",
            "param": "string"
          }
        ],
        "object": "string"
      },
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "failedAt": "2026-05-07T12:00:00.000Z",
      "finalizingAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inProgressAt": "2026-05-07T12:00:00.000Z",
      "inputFileId": "string",
      "metadata": "2026-05-07T12:00:00.000Z",
      "model": {},
      "object": "string",
      "outputFileId": {},
      "requestCounts": {
        "completed": "2026-05-07T12:00:00.000Z",
        "failed": "2026-05-07T12:00:00.000Z",
        "total": "2026-05-07T12:00:00.000Z"
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
| `errors.data[].code` | string |  |
| `errors.data[].line` | object |  |
| `errors.data[].message` | string |  |
| `errors.data[].param` | string |  |
| `errors.object` | string |  |
| `expiredAt` | date |  |
| `expiresAt` | date |  |
| `failedAt` | date |  |
| `finalizingAt` | date |  |
| `id` | string |  |
| `inProgressAt` | date |  |
| `inputFileId` | string |  |
| `metadata` | date |  |
| `model` | object |  |
| `object` | string |  |
| `outputFileId` | object |  |
| `requestCounts.completed` | date |  |
| `requestCounts.failed` | date |  |
| `requestCounts.total` | date |  |
| `status` | string |  |
| `usage.inputTokens` | number |  |
| `usage.inputTokensDetails.cachedTokens` | number |  |
| `usage.outputTokens` | number |  |
| `usage.outputTokensDetails.reasoningTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/batches/:batch_id` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-batch.md) for the provider-specific parameters and requirements.

