# Crossmint: Create Transaction

Creates a transaction in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletLocator": "email:user@example.com:evm-smart-wallet",
  "params.calls[0].to": "0x0000000000000000000000000000000000000000",
  "params.calls[0].value": "0x0",
  "params.calls[0].data": "0x",
  "params.chain": "base-sepolia",
  "params.signer": "external-wallet:0xYourSignerAddress"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletLocator": "email:user@example.com:evm-smart-wallet",
    "params.calls[0].to": "0x0000000000000000000000000000000000000000",
    "params.calls[0].value": "0x0",
    "params.calls[0].data": "0x",
    "params.chain": "base-sepolia",
    "params.signer": "external-wallet:0xYourSignerAddress"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletLocator` | string | yes | Wallet locator or wallet address from the Crossmint wallet locator formats. Example: `email:user@example.com:evm-smart-wallet`. |
| `params.calls[0].to` | string | yes | Destination address for the EVM call. Example: `0x0000000000000000000000000000000000000000`. |
| `params.calls[0].value` | string | yes | Hex-encoded wei value for the EVM call. Default: `0x0`. |
| `params.calls[0].data` | string | yes | Hex calldata for the EVM call. Default: `0x`. |
| `params.chain` | string | yes | Target EVM chain for the transaction. Default: `base-sepolia`. |
| `params.signer` | string | yes | Signer identifier used to approve the transaction. Example: `external-wallet:0xYourSignerAddress`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2025-06-09/wallets/:walletLocator/transactions` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

