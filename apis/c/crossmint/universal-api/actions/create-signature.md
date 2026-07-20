# Crossmint: Create Signature

Creates a signature in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-signature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletLocator": "email:user@example.com:evm:smart",
  "type": "message",
  "params.message": "Hello, world!",
  "params.signer": "external-wallet:0xYourSignerAddress",
  "params.chain": "base-sepolia"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-signature', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletLocator": "email:user@example.com:evm:smart",
    "type": "message",
    "params.message": "Hello, world!",
    "params.signer": "external-wallet:0xYourSignerAddress",
    "params.chain": "base-sepolia"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletLocator` | string | yes | Wallet locator using the Crossmint wallet locator formats. Example: `email:user@example.com:evm:smart`. |
| `type` | string | yes | Signature type. Default: `message`. |
| `params.message` | string | yes | Message to sign. Example: `Hello, world!`. |
| `params.signer` | string | yes | Signer identifier used to approve the signature. Example: `external-wallet:0xYourSignerAddress`. |
| `params.chain` | string | yes | Target chain for the signature context. Default: `base-sepolia`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2025-06-09/wallets/:walletLocator/signatures` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signature.md) for the provider-specific parameters and requirements.

