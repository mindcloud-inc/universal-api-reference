# Becon: Get Balance

Retrieves BTC wallet balances from Becon by address.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-balance?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-balance?${params}`, {
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
| `address` | string | yes | Whitespace-separated wallet addresses to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "balance": "string",
      "balance_bonus": "string",
      "created_at": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Wallet address. |
| `balance` | string | Confirmed balance amount. |
| `balance_bonus` | string | Pending or bonus balance amount. |
| `created_at` | string | Wallet creation timestamp. |
| `id` | number | Wallet balance row id. |

## Native endpoint

Through the native Becon API, this operation is `GET /v1/user/balance` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.

