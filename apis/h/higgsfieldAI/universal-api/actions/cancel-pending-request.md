# Higgsfield AI: Cancel Pending Request

Cancels a pending generation request in Higgsfield AI.

```
PUT https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/cancel-pending-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Higgsfield AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/cancel-pending-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/cancel-pending-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Queued Higgsfield request UUID to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "request_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `request_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Higgsfield AI API, this operation is `POST /requests/{requestId}/cancel` (base URL `https://platform.higgsfield.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-pending-request.md) for the provider-specific parameters and requirements.

