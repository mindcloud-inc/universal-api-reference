# Crossmint: Transfer Token

Transfers a token from a Crossmint wallet.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/transfer-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/transfer-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletLocator": "email:user@example.com:evm:smart",
  "tokenLocator": "base-sepolia:usdxm",
  "recipient": "0x1234567890123456789012345678901234567890",
  "amount": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/transfer-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletLocator": "email:user@example.com:evm:smart",
    "tokenLocator": "base-sepolia:usdxm",
    "recipient": "0x1234567890123456789012345678901234567890",
    "amount": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletLocator` | string | yes | Wallet locator using the Crossmint wallet locator formats. Example: `email:user@example.com:evm:smart`. |
| `tokenLocator` | string | yes | Token locator like chain:currency or chain:address. Default: `base-sepolia:usdxm`. |
| `recipient` | string | yes | Recipient locator or wallet address. Example: `0x1234567890123456789012345678901234567890`. |
| `signer` | string | no | Optional signer locator. Defaults to the admin signer. Example: `external-wallet:0xYourSignerAddress`. |
| `amount` | string | yes | Decimal token amount to transfer. Default: `1`. |
| `transactionType` | string | no | Transfer transaction type. Default: `direct`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2025-06-09/wallets/:walletLocator/tokens/:tokenLocator/transfers` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-token.md) for the provider-specific parameters and requirements.

