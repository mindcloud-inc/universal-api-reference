# GoAffPro: Recalculate Order Commission

Recalculates commission for an order in GoAffPro.

```
PUT https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/recalculate-order-commission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/recalculate-order-commission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/recalculate-order-commission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commission": 1,
      "orderId": "string",
      "subtotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commission` | number | Recalculated commission. |
| `orderId` | string | Recalculated order ID. |
| `subtotal` | number | Recalculated subtotal. |

## Native endpoint

Through the native GoAffPro API, this operation is `POST /admin/orders/recalculate/:id` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recalculate-order-commission.md) for the provider-specific parameters and requirements.

