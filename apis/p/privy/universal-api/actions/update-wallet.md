# Privy: Update Wallet

Updates an existing wallet in Privy.

```
PUT https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-wallet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletId` | string | yes | Privy wallet ID. |

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

Through the native Privy API, this operation is `PATCH /v1/wallets/{{walletId}}` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-wallet.md) for the provider-specific parameters and requirements.

