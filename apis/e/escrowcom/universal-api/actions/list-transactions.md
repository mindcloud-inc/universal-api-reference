# Escrow.com: List Transactions

Retrieves transaction records from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-transactions?${params}`, {
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
      "closeDate": "2026-05-07T12:00:00.000Z",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "id": 1,
      "items": [
        {}
      ],
      "parties": [
        {}
      ],
      "partnerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closeDate` | date | Transaction close timestamp when available. |
| `creationDate` | date | Transaction creation timestamp. |
| `currency` | string | Transaction currency code. |
| `description` | string | Transaction description. |
| `id` | number | Escrow.com transaction ID. |
| `items` | array<object> | Milestone or general merchandise items in the transaction. |
| `parties` | array<object> | Buyer, seller, broker, and partner parties on the transaction. |
| `partnerId` | number | Partner identifier associated with the transaction when available. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

