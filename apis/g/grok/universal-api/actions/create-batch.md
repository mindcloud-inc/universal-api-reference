# Grok: Create Batch

Creates a new batch in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchRequests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchRequests[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchName` | string | no | Optional human-readable batch name. |
| `batchRequests[]` | array<object> | yes | Requests to include in the new batch. |

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

Through the native Grok API, this operation is `POST /v1/batches` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch.md) for the provider-specific parameters and requirements.

