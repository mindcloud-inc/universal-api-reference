# Crossmint: List Wallet Transfers

Retrieves wallet transfer activity from Crossmint.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-wallet-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-wallet-transfers?connectionId=$CONNECTION_ID&walletLocator=email%3Auser%40example.com%3Aevm%3Asmart&chain=base-sepolia&tokens=base-sepolia%3Ausdxm&status=successful" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletLocator": "email:user@example.com:evm:smart",
  "chain": "base-sepolia",
  "tokens": "base-sepolia:usdxm",
  "status": "successful"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-wallet-transfers?${params}`, {
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
| `chain` | string | yes | Blockchain network to query. Default: `base-sepolia`. |
| `tokens` | string | yes | Comma-separated list of tokens or token locator strings. Default: `base-sepolia:usdxm`. |
| `status` | string | yes | Transfer status to query. Default: `successful`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `GET /unstable/wallets/:walletLocator/transfers` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wallet-transfers.md) for the provider-specific parameters and requirements.

