# GoAffPro: Create Order

Creates a manual affiliate order and commission in GoAffPro.

```
POST https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order.number": "string",
  "order.total": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order.number": "string",
    "order.total": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order.number` | string | yes | Order number to display. |
| `order.total` | number | yes | Total order value. |
| `affiliateId` | string | no | Affiliate ID to assign the order to. |
| `refCode` | string | no | Referral code used in the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": "string",
      "commission": 1,
      "data": {
        "currency": "string",
        "id": "string",
        "number": "string",
        "orderStatus": "string",
        "total": 1
      },
      "qv": 1,
      "subtotal": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | string | Affiliate ID associated with the order. |
| `commission` | number | Calculated commission for the created order. |
| `data.currency` | string | Created order currency. |
| `data.id` | string | Created order ID. |
| `data.number` | string | Created order number. |
| `data.orderStatus` | string | Created order status. |
| `data.total` | number | Created order total. |
| `qv` | number | Order qualifying volume. |
| `subtotal` | number | Order subtotal used for commission calculation. |
| `total` | number | Order total used for commission calculation. |

## Native endpoint

Through the native GoAffPro API, this operation is `POST /admin/orders` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

