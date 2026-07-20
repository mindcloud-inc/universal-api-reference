# Grok: Get Batch

Retrieves a specific batch from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-batch?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-batch?${params}`, {
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
| `batchId` | string | yes | Batch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "createTime": "string",
      "name": "Ava Chen",
      "state": {
        "numCancelled": 1,
        "numError": 1,
        "numPending": 1,
        "numRequests": 1,
        "numSuccess": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string | Batch identifier. |
| `createTime` | string | Timestamp when the batch was created. |
| `name` | string | Batch name. |
| `state` | object | Current batch state and counters. |
| `state.numCancelled` | number | Number of requests that were cancelled. |
| `state.numError` | number | Number of requests that failed. |
| `state.numPending` | number | Number of requests still pending. |
| `state.numRequests` | number | Total number of requests in the batch. |
| `state.numSuccess` | number | Number of requests that completed successfully. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/batches/:batch_id` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch.md) for the provider-specific parameters and requirements.

