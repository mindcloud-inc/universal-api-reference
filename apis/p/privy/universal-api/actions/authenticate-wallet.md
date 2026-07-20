# Privy: Authenticate Wallet

Authenticates a wallet session in Privy.

```
POST https://connect.mindcloud.co/v1/universal/privy/latest/actions/authenticate-wallet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/authenticate-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/authenticate-wallet', {
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
      "encrypted_authorization_key": {
        "ciphertext": "string",
        "encapsulated_key": "string",
        "encryption_type": "string"
      },
      "expires_at": 1,
      "wallets": [
        {
          "address": "string",
          "chain_type": "string",
          "created_at": 1,
          "id": "string"
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
| `encrypted_authorization_key.ciphertext` | string |  |
| `encrypted_authorization_key.encapsulated_key` | string |  |
| `encrypted_authorization_key.encryption_type` | string |  |
| `expires_at` | number |  |
| `wallets[].address` | string |  |
| `wallets[].chain_type` | string |  |
| `wallets[].created_at` | number |  |
| `wallets[].id` | string |  |

## Native endpoint

Through the native Privy API, this operation is `POST /v1/wallets/authenticate` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate-wallet.md) for the provider-specific parameters and requirements.

