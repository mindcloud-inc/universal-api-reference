# Rye: Purchase Product

Creates a product purchase in Rye.

```
POST https://connect.mindcloud.co/v1/universal/rye/latest/actions/purchase-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rye/latest/actions/purchase-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "buyer": {},
  "paymentMethod": {},
  "productUrl": "https://example.com",
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rye/latest/actions/purchase-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "buyer": {},
    "paymentMethod": {},
    "productUrl": "https://example.com",
    "quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buyer` | object | yes | Buyer information object. |
| `constraints` | object | no | Checkout constraints object. |
| `discoverPromoCodes` | boolean | no | Whether to discover promo codes automatically. |
| `paymentMethod` | object | yes | Payment method object. |
| `productUrl` | string | yes | Product URL to purchase. |
| `promoCodes[]` | array<string> | no | Promo codes to apply. Accepts multiple values as an array. |
| `quantity` | number | yes | Quantity to purchase. |
| `variantSelections[]` | array<object> | no | Variant selections to apply. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyer": {},
      "constraints": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discoverPromoCodes": true,
      "failureReason": {},
      "id": "string",
      "nextAction": {},
      "offer": {},
      "orderId": "string",
      "paymentMethod": {},
      "productUrl": "https://example.com",
      "promoCodes": [
        "string"
      ],
      "quantity": 1,
      "state": "string",
      "variantSelections": [
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
| `buyer` | object |  |
| `constraints` | object |  |
| `createdAt` | date |  |
| `discoverPromoCodes` | boolean |  |
| `failureReason` | object |  |
| `id` | string |  |
| `nextAction` | object |  |
| `offer` | object |  |
| `orderId` | string |  |
| `paymentMethod` | object |  |
| `productUrl` | string |  |
| `promoCodes` | array<string> |  |
| `quantity` | number |  |
| `state` | string |  |
| `variantSelections` | array<object> |  |

## Native endpoint

Through the native Rye API, this operation is `POST /api/v1/checkout-intents/purchase` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-product.md) for the provider-specific parameters and requirements.

