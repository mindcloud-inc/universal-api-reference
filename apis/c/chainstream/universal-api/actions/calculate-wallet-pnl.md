# Chainstream: Calculate Wallet PnL

Calculates wallet token PnL in Chainstream.

```
POST https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/calculate-wallet-pnl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/calculate-wallet-pnl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "string",
  "walletAddress": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/calculate-wallet-pnl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "string",
    "walletAddress": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chain` | string | yes | A chain name listed in supported networks. |
| `walletAddress` | string | yes | An address of a wallet. |
| `tokenAddresses[]` | array<string> | no | Token addresses to include in the calculation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Chainstream API, this operation is `POST /v2/wallet/:chain/:walletAddress/calculate-pnl` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-wallet-pnl.md) for the provider-specific parameters and requirements.

