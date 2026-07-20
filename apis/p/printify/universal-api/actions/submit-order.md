# Printify: Submit Order

Submits an order to Printify.

```
POST https://connect.mindcloud.co/v1/universal/printify/latest/actions/submit-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printify/latest/actions/submit-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address_to": {},
  "line_items": {},
  "shipping_method": "1",
  "shop_id": "27141936"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/submit-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address_to": {},
    "line_items": {},
    "shipping_method": "1",
    "shop_id": "27141936"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address_to` | object | yes | Recipient shipping address. |
| `line_items` | list<object> | yes | Order line items. |
| `shipping_method` | number | yes | Shipping method code. Default: `1`. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appOrderId": "string",
      "createdAt": "string",
      "fulfilmentType": "string",
      "id": "string",
      "shippingMethod": 1,
      "status": "string",
      "totalPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appOrderId` | string |  |
| `createdAt` | string |  |
| `fulfilmentType` | string |  |
| `id` | string |  |
| `shippingMethod` | number |  |
| `status` | string |  |
| `totalPrice` | number |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/orders.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-order.md) for the provider-specific parameters and requirements.

