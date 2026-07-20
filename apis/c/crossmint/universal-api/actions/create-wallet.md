# Crossmint: Create Wallet

Creates a new wallet in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chainType": "evm",
  "config.adminSigner.type": "external-wallet",
  "config.adminSigner.address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-wallet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chainType": "evm",
    "config.adminSigner.type": "external-wallet",
    "config.adminSigner.address": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chainType` | string | yes | Blockchain type for the wallet. Example: evm. Default: `evm`. |
| `type` | string | no | Wallet type. Example: smart. Default: `smart`. |
| `config.adminSigner.type` | string | yes | Admin signer type for EVM smart wallets. Example: external-wallet. Default: `external-wallet`. |
| `config.adminSigner.address` | string | yes | Admin signer wallet address for EVM smart wallets. |
| `owner` | string | no | Wallet owner locator such as email:user@example.com or COMPANY. Example: `email:user@example.com`. |
| `alias` | string | no | Optional wallet alias. Example: `my-usdc-wallet`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "chainType": "string",
      "config": {},
      "createdAt": "string",
      "owner": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Onchain wallet address. |
| `chainType` | string | Blockchain type of the wallet. |
| `config` | object | Wallet configuration including admin signer details. |
| `createdAt` | string | Wallet creation timestamp. |
| `owner` | string | Owner locator for the wallet. |
| `type` | string | Wallet type. |

## Native endpoint

Through the native Crossmint API, this operation is `POST /2025-06-09/wallets` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wallet.md) for the provider-specific parameters and requirements.

