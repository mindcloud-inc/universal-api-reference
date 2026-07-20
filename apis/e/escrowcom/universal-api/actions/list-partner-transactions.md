# Escrow.com: List Partner Transactions

Retrieves partner transactions from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-partner-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-partner-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/list-partner-transactions?${params}`, {
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
| `limit` | number | no | Maximum partner transactions to fetch. |
| `nextCursor` | number | no | Cursor to start fetching partner transactions from. |
| `sortBy` | string | no | Partner transaction sort field. |
| `sortDirection` | string | no | Sort direction, asc or desc. |

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

Through the native Escrow.com API, this operation is `GET /partner/transactions` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-partner-transactions.md) for the provider-specific parameters and requirements.

