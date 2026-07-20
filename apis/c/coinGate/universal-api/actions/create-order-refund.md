# CoinGate: Create Order Refund

Creates a refund for a specific CoinGate order.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-order-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-order-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "amount": 1,
  "address": "string",
  "currencyId": 1,
  "platformId": 1,
  "reason": "string",
  "email": "ava@example.com",
  "ledgerAccountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-order-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1,
    "amount": 1,
    "address": "string",
    "currencyId": 1,
    "platformId": 1,
    "reason": "string",
    "email": "ava@example.com",
    "ledgerAccountId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | CoinGate order ID. |
| `amount` | number | yes | Refund amount. |
| `address` | string | yes | Refund destination address. |
| `currencyId` | number | yes | CoinGate currency ID. |
| `platformId` | number | yes | CoinGate platform ID. |
| `reason` | string | yes | Refund reason. |
| `email` | string | yes | Refund contact email. |
| `ledgerAccountId` | string | yes | CoinGate ledger account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "id": 1,
      "refundAmount": "string",
      "requestAmount": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `id` | number |  |
| `refundAmount` | string |  |
| `requestAmount` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /orders/:order_id/refunds` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-refund.md) for the provider-specific parameters and requirements.

