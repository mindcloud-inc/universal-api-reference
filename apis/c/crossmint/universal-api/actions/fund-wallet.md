# Crossmint: Fund Wallet

Funds a wallet in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/fund-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/fund-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletLocator": "email:user@example.com:evm-smart-wallet",
  "amount": "10",
  "token": "usdxm",
  "chain": "base-sepolia"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/fund-wallet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletLocator": "email:user@example.com:evm-smart-wallet",
    "amount": "10",
    "token": "usdxm",
    "chain": "base-sepolia"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletLocator` | string | yes | Wallet locator such as a wallet address or email:user@example.com:evm-smart-wallet. Example: `email:user@example.com:evm-smart-wallet`. |
| `amount` | number | yes | Amount to fund, between 1 and 100. Default: `10`. |
| `token` | string | yes | Funding token. Only usdxm is supported in staging. Default: `usdxm`. |
| `chain` | string | yes | Chain to fund on. Example: base-sepolia. Default: `base-sepolia`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "txId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `txId` | string | Funding transaction identifier returned by the runtime. |

## Native endpoint

Through the native Crossmint API, this operation is `POST /v1-alpha2/wallets/:walletLocator/balances` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fund-wallet.md) for the provider-specific parameters and requirements.

