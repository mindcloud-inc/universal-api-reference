# Order Desk: Get Order

Retrieves an order from Order Desk.

```
GET https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-order?${params}`, {
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
| `orderId` | string | yes | Order Desk internal order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {},
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "discountTotal": 1,
      "email": "ava@example.com",
      "folderId": 1,
      "handlingTotal": 1,
      "id": "string",
      "orderItems": [
        {}
      ],
      "orderShipments": [
        {}
      ],
      "orderTotal": 1,
      "paymentStatus": "string",
      "paymentType": "string",
      "productTotal": 1,
      "quantityTotal": 1,
      "shipping": {},
      "shippingMethod": "string",
      "shippingTotal": 1,
      "sourceId": "string",
      "sourceName": "Ava Chen",
      "taxTotal": 1,
      "weightTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object | Customer address details. |
| `dateAdded` | date | Order creation timestamp in UTC. |
| `dateUpdated` | date | Last update timestamp in UTC. |
| `discountTotal` | number | Discount total. |
| `email` | string | Customer email address. |
| `folderId` | number | Current folder ID. |
| `handlingTotal` | number | Handling total. |
| `id` | string | Order Desk internal order ID. |
| `orderItems` | array<object> | Order line items. |
| `orderShipments` | array<object> | Order shipments. |
| `orderTotal` | number | Final order total. |
| `paymentStatus` | string | Payment status. |
| `paymentType` | string | Payment method type. |
| `productTotal` | number | Product subtotal. |
| `quantityTotal` | number | Total quantity across order items. |
| `shipping` | object | Shipping address details. |
| `shippingMethod` | string | Shipping method name. |
| `shippingTotal` | number | Shipping total. |
| `sourceId` | string | Order source ID. |
| `sourceName` | string | Order source name. |
| `taxTotal` | number | Tax total. |
| `weightTotal` | number | Total order weight. |

## Native endpoint

Through the native Order Desk API, this operation is `GET /orders/:orderId` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

