# CoinGate: Get Order Transaction

Retrieves a blockchain transaction for a CoinGate order.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-order-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-order-transaction?connectionId=$CONNECTION_ID&orderId=1&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-order-transaction?${params}`, {
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
| `id` | string | yes | CoinGate blockchain transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "id": 1,
      "networkConfirmations": 1,
      "status": "string",
      "txid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `id` | number |  |
| `networkConfirmations` | number |  |
| `status` | string |  |
| `txid` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /orders/:order_id/blockchain_transactions/:id` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-transaction.md) for the provider-specific parameters and requirements.

