# Shipday: Set Order Ready to Pickup

Marks an existing order ready for pickup in Shipday.

```
PUT https://connect.mindcloud.co/v1/universal/shipday/latest/actions/set-order-ready-to-pickup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/set-order-ready-to-pickup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "44865172",
  "readyToPickup": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipday/latest/actions/set-order-ready-to-pickup', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "44865172",
    "readyToPickup": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | Shipday order ID used in the request path. Example: `44865172`. |
| `readyToPickup` | boolean | yes | Pickup-ready status sent in the request body. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shipday API returns.

## Native endpoint

Through the native Shipday API, this operation is `PUT /orders/:orderId/meta` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-order-ready-to-pickup.md) for the provider-specific parameters and requirements.

