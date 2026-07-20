# Crossmint: Create Delegated Signer

Creates a delegated signer in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-delegated-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-delegated-signer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletLocator": "email:user@example.com:evm:smart",
  "signer": "external-wallet:0x1234567890123456789012345678901234567890",
  "chain": "base-sepolia"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-delegated-signer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletLocator": "email:user@example.com:evm:smart",
    "signer": "external-wallet:0x1234567890123456789012345678901234567890",
    "chain": "base-sepolia"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletLocator` | string | yes | Wallet locator using the Crossmint wallet locator formats. Example: `email:user@example.com:evm:smart`. |
| `signer` | string | yes | Signer to register as a delegated signer. Example: `external-wallet:0x1234567890123456789012345678901234567890`. |
| `chain` | string | yes | Chain where the signer will be registered. Default: `base-sepolia`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expiresAt` | string | no | Optional ISO 8601 expiry time for the signer. Example: `2026-12-31T23:59:59.000Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2025-06-09/wallets/:walletLocator/signers` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-delegated-signer.md) for the provider-specific parameters and requirements.

