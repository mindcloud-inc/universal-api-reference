# CoinGate: List Ledger Transactions

Retrieves ledger transactions from your CoinGate account.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-ledger-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-ledger-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-ledger-transactions?${params}`, {
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
      "currentPage": 1,
      "entries": [
        {
          "id": "string"
        }
      ],
      "perPage": 1,
      "totalEntries": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `entries[].id` | string |  |
| `perPage` | number |  |
| `totalEntries` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /ledger/transactions` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ledger-transactions.md) for the provider-specific parameters and requirements.

