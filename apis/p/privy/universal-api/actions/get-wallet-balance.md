# Privy: Get Wallet Balance

Retrieves a wallet balance from Privy.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-wallet-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-wallet-balance?connectionId=$CONNECTION_ID&walletId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-wallet-balance?${params}`, {
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
| `walletId` | string | yes | Privy wallet ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asset` | string | no | Optional asset filter for the balance request. |
| `chain` | string | no | Optional chain filter for the balance request. |
| `includeCurrency` | string | no | Optional fiat currency code to include valuation data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balances": [
        {
          "asset": "string",
          "chain": "string",
          "display_values": {},
          "raw_value": "string",
          "raw_value_decimals": 1
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
| `balances[].asset` | string |  |
| `balances[].chain` | string |  |
| `balances[].display_values` | object |  |
| `balances[].raw_value` | string |  |
| `balances[].raw_value_decimals` | number |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/wallets/{{walletId}}/balance` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-balance.md) for the provider-specific parameters and requirements.

