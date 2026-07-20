# Torque: Get Wallet PnL



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-wallet-pnl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-wallet-pnl?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-wallet-pnl?${params}`, {
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
| `address` | string | yes | Wallet address to query. |
| `chain` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total_bought_volume_usd": 1,
      "total_buys": 1,
      "total_count_of_trades": 1,
      "total_realized_profit_percentage": 1,
      "total_realized_profit_usd": 1,
      "total_sells": 1,
      "total_sold_volume_usd": 1,
      "total_trade_volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total_bought_volume_usd` | number |  |
| `total_buys` | number |  |
| `total_count_of_trades` | number |  |
| `total_realized_profit_percentage` | number |  |
| `total_realized_profit_usd` | number |  |
| `total_sells` | number |  |
| `total_sold_volume_usd` | number |  |
| `total_trade_volume` | number |  |

## Native endpoint

Through the native Torque API, this operation is `GET /moralis/wallet-pnl` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-pnl.md) for the provider-specific parameters and requirements.

