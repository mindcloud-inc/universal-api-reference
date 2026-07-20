# Strale: List Wallet Transactions

Retrieves wallet transactions from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-wallet-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-wallet-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-wallet-transactions?${params}`, {
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
      "amountCents": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountCents` | number | Wallet transaction amount in cents. |
| `createdAt` | date | Wallet transaction creation timestamp. |
| `description` | string | Wallet transaction description. |
| `id` | string | Wallet transaction identifier. |
| `type` | string | Wallet transaction type. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/wallet/transactions` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wallet-transactions.md) for the provider-specific parameters and requirements.

