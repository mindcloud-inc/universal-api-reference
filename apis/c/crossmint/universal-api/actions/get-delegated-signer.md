# Crossmint: Get Delegated Signer

Retrieves a delegated signer from Crossmint.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-delegated-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-delegated-signer?connectionId=$CONNECTION_ID&walletLocator=email%3Auser%40example.com%3Aevm%3Asmart&signer=external-wallet%3A0x1234567890123456789012345678901234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletLocator": "email:user@example.com:evm:smart",
  "signer": "external-wallet:0x1234567890123456789012345678901234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-delegated-signer?${params}`, {
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
| `walletLocator` | string | yes | Wallet locator using the Crossmint wallet locator formats. Example: `email:user@example.com:evm:smart`. |
| `signer` | string | yes | Signer locator. Example: `external-wallet:0x1234567890123456789012345678901234567890`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `GET /2025-06-09/wallets/:walletLocator/signers/:signer` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delegated-signer.md) for the provider-specific parameters and requirements.

