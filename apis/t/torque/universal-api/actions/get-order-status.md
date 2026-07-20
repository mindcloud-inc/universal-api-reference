# Torque: Get Order Status



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-order-status?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-order-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Torque checkout order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "customer": {},
      "items": [
        {}
      ],
      "metadata": {},
      "orderId": "string",
      "paymentStatus": "string",
      "shippingAddress": {
        "city": "string",
        "country": "string",
        "state": "string",
        "street": "string",
        "zip": "string"
      },
      "status": "string",
      "totals": {
        "shipping": 1,
        "subtotal": 1,
        "tax": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Order creation timestamp returned by Torque. |
| `customer` | object | Customer details when returned by Torque. |
| `items` | array<object> | Line items included in the order. |
| `metadata` | object | Additional order metadata. |
| `orderId` | string | Torque checkout order ID. |
| `paymentStatus` | string | Payment status for the order. |
| `shippingAddress` | object | Shipping address for the order. |
| `shippingAddress.city` | string | Shipping city. |
| `shippingAddress.country` | string | Shipping country code. |
| `shippingAddress.state` | string | Shipping state or region. |
| `shippingAddress.street` | string | Shipping street address. |
| `shippingAddress.zip` | string | Shipping postal code. |
| `status` | string | Current order status. |
| `totals` | object | Order subtotal, shipping, tax, and total amounts. |
| `totals.shipping` | number | Shipping amount. |
| `totals.subtotal` | number | Order subtotal amount. |
| `totals.tax` | number | Tax amount. |
| `totals.total` | number | Total order amount. |

## Native endpoint

Through the native Torque API, this operation is `GET /checkout/order-status/:orderId` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-status.md) for the provider-specific parameters and requirements.

