# CoinGate: List Order Transactions

Retrieves blockchain transactions for a specific CoinGate order.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-order-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-order-transactions?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-order-transactions?${params}`, {
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
| `orderId` | number | yes | CoinGate order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "perPage": 1,
      "totalPages": 1,
      "totalTransactions": 1,
      "transactions": [
        {
          "id": 1
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
| `currentPage` | number |  |
| `perPage` | number |  |
| `totalPages` | number |  |
| `totalTransactions` | number |  |
| `transactions[].id` | number |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /orders/:order_id/blockchain_transactions` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-transactions.md) for the provider-specific parameters and requirements.

