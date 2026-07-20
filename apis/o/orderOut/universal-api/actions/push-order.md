# OrderOut: Push Order

Pushes an order from a channel to OrderOut.

```
POST https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/push-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OrderOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/push-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rawBody": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/push-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rawBody": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rawBody` | string | yes | Order payload JSON string |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OrderOut API returns.

## Native endpoint

Through the native OrderOut API, this operation is `POST /api/channel/order/push` (base URL `https://api.orderout.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/push-order.md) for the provider-specific parameters and requirements.

