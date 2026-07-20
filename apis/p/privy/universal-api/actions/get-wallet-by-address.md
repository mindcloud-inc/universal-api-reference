# Privy: Get Wallet By Address

Finds a wallet in Privy by address.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-wallet-by-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-wallet-by-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-wallet-by-address?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "chain_type": "string",
      "created_at": 1,
      "display_name": "Ava Chen",
      "external_id": "string",
      "id": "string",
      "owner_id": "string",
      "policy_ids": [
        "string"
      ],
      "public_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `chain_type` | string |  |
| `created_at` | number |  |
| `display_name` | string |  |
| `external_id` | string |  |
| `id` | string |  |
| `owner_id` | string |  |
| `policy_ids` | array<string> |  |
| `public_key` | string |  |

## Native endpoint

Through the native Privy API, this operation is `POST /v1/wallets/address` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-by-address.md) for the provider-specific parameters and requirements.

