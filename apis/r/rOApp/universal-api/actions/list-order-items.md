# RO App: List Order Items



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-order-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-order-items?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-order-items?${params}`, {
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
| `orderId` | number | yes | Order ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee_id": 1,
      "comment": "string",
      "cost": 1,
      "discount": {
        "amount": 1,
        "percentage": 1,
        "sponsor": "string",
        "type": "string"
      },
      "entity_id": 1,
      "price": 1,
      "quantity": 1,
      "tax_ids": [
        1
      ],
      "warranty": {
        "period": "string",
        "periodUnits": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee_id` | number |  |
| `comment` | string |  |
| `cost` | number |  |
| `discount` | object |  |
| `discount.amount` | number |  |
| `discount.percentage` | number |  |
| `discount.sponsor` | string |  |
| `discount.type` | string |  |
| `entity_id` | number |  |
| `price` | number |  |
| `quantity` | number |  |
| `tax_ids` | array<number> |  |
| `warranty` | object |  |
| `warranty.period` | string |  |
| `warranty.periodUnits` | string |  |

## Native endpoint

Through the native RO App API, this operation is `GET /orders/:order_id/items` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-items.md) for the provider-specific parameters and requirements.

