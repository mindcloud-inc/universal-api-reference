# OrderOut: Create Push Order Webhook

Creates a push order webhook in OrderOut.

```
POST https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-push-order-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OrderOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-push-order-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "string",
  "method": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-push-order-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "string",
    "method": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorizationHeader` | string | no | Optional auth header |
| `endpoint` | string | yes | Webhook URL |
| `method` | string | yes | Webhook method |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OrderOut API returns.

## Native endpoint

Through the native OrderOut API, this operation is `POST /api/webhooks/push_order` (base URL `https://api.orderout.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-push-order-webhook.md) for the provider-specific parameters and requirements.

