# HeyPoplar: Update Order

Updates an existing order in HeyPoplar.

```
PUT https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | The ID of the order to edit. |
| `orderDate` | string | no | ISO8601 purchase date in YYYY-MM-DD format. |
| `customerEmail` | string | no | Customer email address used to identify the order. |
| `total` | number | no | Updated order total. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_address": {},
      "currency": "string",
      "customer": {},
      "id": "string",
      "metadata": {},
      "order_date": "string",
      "order_id": "string",
      "order_items": [
        {}
      ],
      "shipping_address": {},
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_address` | object |  |
| `currency` | string |  |
| `customer` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `order_date` | string |  |
| `order_id` | string |  |
| `order_items` | array<object> |  |
| `shipping_address` | object |  |
| `total` | string |  |

## Native endpoint

Through the native HeyPoplar API, this operation is `POST /order/:order_id` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

