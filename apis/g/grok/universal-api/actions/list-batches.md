# Grok: List Batches

Retrieves a list of batches from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-batches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-batches?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "batches": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batches` | array<object> | Batches visible to the current account. |
| `batches[].batchId` | string | Batch identifier. |
| `batches[].createTime` | string | Timestamp when the batch was created. |
| `batches[].name` | string | Batch name. |
| `batches[].state` | object | Current batch state and counters. |
| `batches[].state.numCancelled` | number | Number of requests that were cancelled. |
| `batches[].state.numError` | number | Number of requests that failed. |
| `batches[].state.numPending` | number | Number of requests still pending. |
| `batches[].state.numRequests` | number | Total number of requests in the batch. |
| `batches[].state.numSuccess` | number | Number of requests that completed successfully. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/batches` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-batches.md) for the provider-specific parameters and requirements.

