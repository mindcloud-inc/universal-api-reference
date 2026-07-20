# RO App: Create Order Item



```
POST https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "entityId": 1,
  "assigneeId": 1,
  "quantity": 1,
  "price": 1,
  "cost": 1,
  "discount": {},
  "discount.type": "string",
  "discount.percentage": 1,
  "discount.amount": 1,
  "discount.sponsor": "string",
  "warranty": {},
  "warranty.period": "string",
  "warranty.periodUnits": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-order-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1,
    "entityId": 1,
    "assigneeId": 1,
    "quantity": 1,
    "price": 1,
    "cost": 1,
    "discount": {},
    "discount.type": "string",
    "discount.percentage": 1,
    "discount.amount": 1,
    "discount.sponsor": "string",
    "warranty": {},
    "warranty.period": "string",
    "warranty.periodUnits": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | Order ID |
| `entityId` | number | yes | Product or Service ID |
| `assigneeId` | number | yes | Assigned Employee ID |
| `quantity` | number | yes | Quantity |
| `price` | number | yes | Price per unit |
| `cost` | number | yes | Unit cost |
| `discount` | object | yes | Item discount object |
| `discount.type` | string | yes | Discount type. "percentage" — percent, "value" — absolute value. |
| `discount.percentage` | number | yes | Percentage value |
| `discount.amount` | number | yes |  |
| `discount.sponsor` | string | yes | "staff" — Employee wages calculation is based on the amount after discount. This way the company discount decreases the piecework employee wages. "company" — Employee commissions will be calculated from amount before discount. This way the company discount won't affect the employee commissions. |
| `warranty` | object | yes | Item warranty object |
| `warranty.period` | string | yes | Warranty period |
| `warranty.periodUnits` | string | yes | Warranty unit of measure |
| `taxIds[]` | array<number> | no | Array of Tax ID |
| `comment` | string | no | Comment text |

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

Through the native RO App API, this operation is `POST /orders/:order_id/items` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-item.md) for the provider-specific parameters and requirements.

