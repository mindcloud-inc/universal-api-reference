# Strale: Get Wallet Balance

Retrieves your wallet balance from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-wallet-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-wallet-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-wallet-balance?${params}`, {
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
      "balanceCents": 1,
      "currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceCents` | number | Wallet balance in cents. |
| `currency` | string | Wallet currency code. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/wallet/balance` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-balance.md) for the provider-specific parameters and requirements.

