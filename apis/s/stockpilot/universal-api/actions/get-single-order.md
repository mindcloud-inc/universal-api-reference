# Stockpilot: Get Single Order

Retrieves an order from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-single-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-single-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-single-order?${params}`, {
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
| `orderPk` | number | no |  |
| `orderNumber` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer_name": "Ava Chen",
      "id": 1,
      "order_details": {
        "customer_email": "ava@example.com",
        "line_items": [
          [
            {}
          ]
        ],
        "shipping_total": "string",
        "total": "string"
      },
      "order_number": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `customer_name` | string |  |
| `id` | number |  |
| `order_details.customer_email` | string |  |
| `order_details.line_items[]` | array<object> |  |
| `order_details.line_items[].id` | number |  |
| `order_details.line_items[].quantity` | number |  |
| `order_details.line_items[].retail_price` | string |  |
| `order_details.shipping_total` | string |  |
| `order_details.total` | string |  |
| `order_number` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /orders/get-single` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-order.md) for the provider-specific parameters and requirements.

