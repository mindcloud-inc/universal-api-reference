# Privy: Create Wallets In Batch

Creates multiple new wallets in Privy.

```
POST https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-wallets-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-wallets-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-wallets-in-batch', {
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
      "results": [
        {
          "index": 1,
          "success": true,
          "wallet": {
            "address": "string",
            "chain_type": "string",
            "created_at": 1,
            "id": "string",
            "policy_ids": [
              "string"
            ]
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].index` | number |  |
| `results[].success` | boolean |  |
| `results[].wallet.address` | string |  |
| `results[].wallet.chain_type` | string |  |
| `results[].wallet.created_at` | number |  |
| `results[].wallet.id` | string |  |
| `results[].wallet.policy_ids` | array<string> |  |

## Native endpoint

Through the native Privy API, this operation is `POST /v1/wallets/batch` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wallets-in-batch.md) for the provider-specific parameters and requirements.

