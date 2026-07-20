# CoinGate: List Ledger Accounts

Retrieves ledger accounts from your CoinGate account.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-ledger-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-ledger-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-ledger-accounts?${params}`, {
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
      "accounts": [
        {
          "id": "string"
        }
      ],
      "currentPage": 1,
      "perPage": 1,
      "totalAccounts": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts[].id` | string |  |
| `currentPage` | number |  |
| `perPage` | number |  |
| `totalAccounts` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /ledger/accounts` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ledger-accounts.md) for the provider-specific parameters and requirements.

