# Chainstream: Get Wallet PnL

Retrieves wallet PnL from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-pnl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-pnl?connectionId=$CONNECTION_ID&chain=string&walletAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "walletAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-pnl?${params}`, {
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
| `chain` | string | yes | A chain name listed in supported networks. |
| `walletAddress` | string | yes | An address of a wallet. |
| `resolution` | string | no | PnL time resolution (1d, 7d, 30d, or all). Default: `1d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avgProfitPerTradeInUsd": "string",
      "buyAmountInUsd": "string",
      "buys": "string",
      "losses": "string",
      "realizedProfitInUsd": "string",
      "resolution": "string",
      "sellAmountInUsd": "string",
      "sells": "string",
      "tokens": "string",
      "totalProfitInUsd": "string",
      "totalProfitRatio": "string",
      "totalTrades": "string",
      "unrealizedProfitInUsd": "string",
      "updatedAt": "string",
      "walletAddress": "string",
      "winRate": "string",
      "wins": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgProfitPerTradeInUsd` | string |  |
| `buyAmountInUsd` | string |  |
| `buys` | string |  |
| `losses` | string |  |
| `realizedProfitInUsd` | string |  |
| `resolution` | string |  |
| `sellAmountInUsd` | string |  |
| `sells` | string |  |
| `tokens` | string |  |
| `totalProfitInUsd` | string |  |
| `totalProfitRatio` | string |  |
| `totalTrades` | string |  |
| `unrealizedProfitInUsd` | string |  |
| `updatedAt` | string |  |
| `walletAddress` | string |  |
| `winRate` | string |  |
| `wins` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/wallet/:chain/:walletAddress/pnl` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-pnl.md) for the provider-specific parameters and requirements.

