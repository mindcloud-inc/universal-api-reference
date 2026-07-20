# Crossmint: List NFTs from Wallet

Retrieves NFTs from a Crossmint wallet.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-nfts-from-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-nfts-from-wallet?connectionId=$CONNECTION_ID&identifier=base-sepolia%3A0x1234567890123456789012345678901234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "base-sepolia:0x1234567890123456789012345678901234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-nfts-from-wallet?${params}`, {
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
| `identifier` | string | yes | Wallet identifier or address for the wallet NFT query. Example: `base-sepolia:0x1234567890123456789012345678901234567890`. |
| `page` | string | no | Page index. Default: `1`. |
| `perPage` | string | no | Number of items per page. Default: `20`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `GET /2022-06-09/wallets/:identifier/nfts` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nfts-from-wallet.md) for the provider-specific parameters and requirements.

