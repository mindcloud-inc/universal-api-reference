# Printify: Submit Express Order

Submits a Printify Express order.

```
POST https://connect.mindcloud.co/v1/universal/printify/latest/actions/submit-express-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printify/latest/actions/submit-express-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address_to": {},
  "line_items": {},
  "shipping_method": "3",
  "shop_id": "27141936"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/submit-express-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address_to": {},
    "line_items": {},
    "shipping_method": "3",
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
| `line_items` | list<object> | yes | Express-order line items. |
| `shipping_method` | number | yes | Shipping method code. Default: `3`. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "appOrderId": "string",
            "fulfilmentType": "string"
          },
          "id": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].attributes` | object |  |
| `data[].attributes.appOrderId` | string |  |
| `data[].attributes.fulfilmentType` | string |  |
| `data[].id` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/orders/express.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-express-order.md) for the provider-specific parameters and requirements.

