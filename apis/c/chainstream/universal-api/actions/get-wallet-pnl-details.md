# Chainstream: Get Wallet PnL Details

Retrieves wallet PnL details from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-pnl-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-pnl-details?connectionId=$CONNECTION_ID&chain=string&walletAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "walletAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-wallet-pnl-details?${params}`, {
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
| `limit` | number | no | Number of results per page. Default: `20`. |
| `direction` | string | no | Pagination direction (next or prev). Default: `next`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "avgProfitPerTradeInUsd": "string",
          "currentValue": "string",
          "logoUri": "string",
          "name": "Ava Chen",
          "symbol": "string",
          "tokenAddress": "string",
          "totalProfitInUsd": "string",
          "walletAddress": "string"
        }
      ],
      "endCursor": "string",
      "hasNext": true,
      "hasPrev": true,
      "startCursor": "string",
      "summary": {
        "avgProfitPerTradeInUsd": "string",
        "totalProfitInUsd": "string",
        "winRate": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].avgProfitPerTradeInUsd` | string |  |
| `data[].currentValue` | string |  |
| `data[].logoUri` | string |  |
| `data[].name` | string |  |
| `data[].symbol` | string |  |
| `data[].tokenAddress` | string |  |
| `data[].totalProfitInUsd` | string |  |
| `data[].walletAddress` | string |  |
| `endCursor` | string |  |
| `hasNext` | boolean |  |
| `hasPrev` | boolean |  |
| `startCursor` | string |  |
| `summary.avgProfitPerTradeInUsd` | string |  |
| `summary.totalProfitInUsd` | string |  |
| `summary.winRate` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/wallet/:chain/:walletAddress/pnl-details` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-pnl-details.md) for the provider-specific parameters and requirements.

