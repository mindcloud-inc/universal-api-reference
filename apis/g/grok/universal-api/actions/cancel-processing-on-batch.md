# Grok: Cancel Processing on Batch

Cancels processing on an existing Grok batch.

```
PUT https://connect.mindcloud.co/v1/universal/grok/latest/actions/cancel-processing-on-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grok/latest/actions/cancel-processing-on-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/cancel-processing-on-batch', {
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
| `batchId` | string | yes | Batch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "state": {
        "numCancelled": 1,
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
| `state` | object | Current batch state and counters after cancellation. |
| `state.numCancelled` | number | Number of requests that were cancelled. |
| `state.numSuccess` | number | Number of requests that completed successfully. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/batches/:batch_id:cancel` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-processing-on-batch.md) for the provider-specific parameters and requirements.

