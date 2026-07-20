# CometAPI: Cancel Message Batch



```
PUT https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/cancel-message-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/cancel-message-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageBatchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/cancel-message-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageBatchId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageBatchId` | string | yes | Message batch ID to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "processing_status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `processing_status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /v1/messages/batches/:message_batch_id/cancel` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-message-batch.md) for the provider-specific parameters and requirements.

