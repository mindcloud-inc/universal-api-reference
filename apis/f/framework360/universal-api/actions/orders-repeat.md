# Framework360: Repeat Order



```
POST https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-repeat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-repeat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "userEmail": "ava@example.com",
  "cart[]": [
    {}
  ],
  "billingData": {},
  "shippingData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-repeat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "userEmail": "ava@example.com",
    "cart[]": [{}],
    "billingData": {},
    "shippingData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Order ID to repeat. |
| `userEmail` | string | yes | User email for the new order. |
| `cart[]` | array<object> | yes | Cart data to reuse for the new order. |
| `billingData` | object | yes | Billing data for the repeated order. |
| `shippingData` | object | yes | Shipping data for the repeated order. |
| `shippingId` | number | no | Shipping method ID. |
| `orderStatus` | number | no | Initial status for the repeated order. |
| `paymentId` | string | no | Payment method ID. |
| `note` | string | no | Additional note for the repeated order. |
| `labels[]` | array<string> | no | Labels to assign to the repeated order. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `POST orders/repeat` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/orders-repeat.md) for the provider-specific parameters and requirements.

