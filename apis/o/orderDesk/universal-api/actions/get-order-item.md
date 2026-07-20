# Order Desk: Get Order Item

Retrieves an order item from Order Desk.

```
GET https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-order-item?connectionId=$CONNECTION_ID&orderId=string&orderItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string",
  "orderItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-order-item?${params}`, {
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
| `orderItemId` | string | yes | Order Desk internal order item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryCode": "string",
      "code": "string",
      "deliveryType": "string",
      "fulfillmentMethod": "string",
      "id": "string",
      "metadata": [
        {}
      ],
      "name": "Ava Chen",
      "price": 1,
      "quantity": 1,
      "variationList": [
        {}
      ],
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryCode` | string | Item category code. |
| `code` | string | Item SKU or code. |
| `deliveryType` | string | Delivery type. |
| `fulfillmentMethod` | string | Fulfillment method. |
| `id` | string | Order Desk internal order item ID. |
| `metadata` | array<object> | Hidden metadata values. |
| `name` | string | Order item name. |
| `price` | number | Item price. |
| `quantity` | number | Item quantity. |
| `variationList` | array<object> | Variation key-value pairs. |
| `weight` | number | Item weight. |

## Native endpoint

Through the native Order Desk API, this operation is `GET /orders/:orderId/order-items/:orderItemId` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-item.md) for the provider-specific parameters and requirements.

