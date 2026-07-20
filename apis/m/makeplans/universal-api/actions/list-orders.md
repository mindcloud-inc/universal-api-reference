# Makeplans: List Orders

Retrieves orders from Makeplans.

```
GET https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-orders?${params}`, {
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
| `state` | string | no | Filter by order state: pending, confirmed, or cancelled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "coupon_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "discount_amount": 1,
      "id": 1,
      "order_line_items": [
        {}
      ],
      "paid_amount": 1,
      "payable_amount": 1,
      "person": {},
      "person_id": 1,
      "settled_at": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "total": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `coupon_id` | number |  |
| `created_at` | date |  |
| `discount_amount` | number |  |
| `id` | number |  |
| `order_line_items` | array<object> |  |
| `paid_amount` | number |  |
| `payable_amount` | number |  |
| `person` | object |  |
| `person_id` | number |  |
| `settled_at` | date |  |
| `state` | string |  |
| `total` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `GET /orders` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

