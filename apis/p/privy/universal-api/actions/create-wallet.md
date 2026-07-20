# Privy: Create Wallet

Creates a new wallet in Privy.

```
POST https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-wallet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Privy API, this operation is `POST /v1/wallets` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wallet.md) for the provider-specific parameters and requirements.

