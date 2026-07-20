# xAI: Cancel Batch

Cancels a batch in the xAI API.

```
PUT https://connect.mindcloud.co/v1/universal/xAI/latest/actions/cancel-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xAI/latest/actions/cancel-batch', {
  method: 'PUT',
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
| `batch_id` | string | no | Batch identifier to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_id": "string",
      "cancel_time": "string",
      "name": "Ava Chen",
      "state": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_id` | string |  |
| `cancel_time` | string |  |
| `name` | string |  |
| `state` | object |  |

## Native endpoint

Through the native xAI API, this operation is `POST /batches/:batch_id:cancel` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-batch.md) for the provider-specific parameters and requirements.

