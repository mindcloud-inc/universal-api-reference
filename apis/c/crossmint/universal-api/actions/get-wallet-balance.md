# Crossmint: Get Wallet Balance

Retrieves a wallet balance from Crossmint.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-wallet-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-wallet-balance?connectionId=$CONNECTION_ID&walletLocator=email%3Auser%40example.com%3Aevm%3Asmart&tokens=base-sepolia%3Ausdxm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletLocator": "email:user@example.com:evm:smart",
  "tokens": "base-sepolia:usdxm"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-wallet-balance?${params}`, {
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
| `tokens` | string | yes | Comma-separated list of tokens or token locators to query. Default: `base-sepolia:usdxm`. |
| `chains` | string | no | Optional comma-separated list of chains to query. Default: `base-sepolia`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `GET /2025-06-09/wallets/:walletLocator/balances` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-balance.md) for the provider-specific parameters and requirements.

