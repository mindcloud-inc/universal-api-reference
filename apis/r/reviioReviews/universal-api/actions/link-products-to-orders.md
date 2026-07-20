# Revi.io Reviews: Link Products to Orders

Links products to orders in Revi.io Reviews.

```
PUT https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/link-products-to-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/link-products-to-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ordersProducts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/link-products-to-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ordersProducts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ordersProducts[]` | array<object> | yes | Array linking each order to one or more purchased products. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order_count": 1,
      "product_count": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order_count` | number | Number of orders linked in this request. |
| `product_count` | number | Number of linked products processed by Revi. |
| `success` | boolean | Whether the order-product link payload was accepted. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `POST /orders_products` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-products-to-orders.md) for the provider-specific parameters and requirements.

