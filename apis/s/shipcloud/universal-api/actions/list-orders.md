# Shipcloud: List Orders

Retrieves orders from Shipcloud.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-orders?${params}`, {
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
| `createdAtGt` | date | no | Return orders created after this date. |
| `createdAtLt` | date | no | Return orders created before this date. |
| `externalCustomerId` | string | no | Filter orders by external customer ID. |
| `externalOrderId` | string | no | Filter orders by external order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "delivery_address": {},
      "external_customer_id": "string",
      "external_order_id": "string",
      "id": "string",
      "order_line_items": [
        {}
      ],
      "placed_at": "2026-05-07T12:00:00.000Z",
      "refundable_until": "2026-05-07T12:00:00.000Z",
      "total_price": 1,
      "total_vat": 1,
      "total_weight": 1,
      "weight_unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `delivery_address` | object |  |
| `external_customer_id` | string |  |
| `external_order_id` | string |  |
| `id` | string |  |
| `order_line_items` | array<object> |  |
| `placed_at` | date |  |
| `refundable_until` | date |  |
| `total_price` | number |  |
| `total_vat` | number |  |
| `total_weight` | number |  |
| `weight_unit` | string |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /orders` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

