# Cratejoy: Create Order

Creates a new order in Cratejoy.

```
POST https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer.id": 1,
  "products[].productInstance.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer.id": 1,
    "products[].productInstance.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.id` | number | yes | The existing Cratejoy customer ID for the order. |
| `shipAddressId` | number | no | The shipping address ID to use for the order. |
| `custPayId` | number | no | The customer's saved payment method ID for the order. |
| `coupons` | string | no | Coupon codes to apply to the order. |
| `products[].productInstance.id` | number | yes | The product instance ID for an order line item. |
| `products[].term.numCycles` | number | no | The number of prepaid cycles for a subscription product term. |
| `products[].quantity` | number | no | The quantity for an order line item. Default: `1`. |
| `orderGiftInfo.giftMessage` | string | no | The gift message for the order gift info. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer_id": 1,
      "financial_status": "string",
      "fulfillment_status": "string",
      "gift_message": "string",
      "id": 1,
      "is_gift": true,
      "placed_at": "2026-05-07T12:00:00.000Z",
      "total": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer_id` | number |  |
| `financial_status` | string |  |
| `fulfillment_status` | string |  |
| `gift_message` | string |  |
| `id` | number |  |
| `is_gift` | boolean |  |
| `placed_at` | date |  |
| `total` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `POST /v1/orders/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

