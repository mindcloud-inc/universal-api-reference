# xAI: Add Batch Requests

Adds batch requests in the xAI API.

```
POST https://connect.mindcloud.co/v1/universal/xAI/latest/actions/add-batch-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/add-batch-requests" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xAI/latest/actions/add-batch-requests', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch_id` | string | no | Batch identifier to add requests to. |
| `batch_requests[]` | array<object> | no | List of batch requests to add to the batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_request_metadata": [
        {}
      ],
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_request_metadata` | array<object> |  |
| `results` | array<object> |  |

## Native endpoint

Through the native xAI API, this operation is `POST /batches/:batch_id/requests` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-batch-requests.md) for the provider-specific parameters and requirements.

