# Trove: Enrich Bulk Transactions

Creates a bulk transaction enrichment request in Trove.

```
POST https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-bulk-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-bulk-transactions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactions[]": [
    {}
  ],
  "transactions[].description": "string",
  "transactions[].amount": 1,
  "transactions[].date": "2026-05-07T12:00:00.000Z",
  "transactions[].user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-bulk-transactions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactions[]": [{}],
    "transactions[].description": "string",
    "transactions[].amount": 1,
    "transactions[].date": "2026-05-07T12:00:00.000Z",
    "transactions[].user_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactions[]` | array<object> | yes | Array of transactions to enrich in bulk. |
| `transactions[].description` | string | yes | The original transaction description string. |
| `transactions[].amount` | number | yes | Transaction value in the original currency. |
| `transactions[].date` | date | yes | The transaction date in YYYY-MM-DD format. |
| `transactions[].user_id` | string | yes | A unique identifier for the customer/user that performed this transaction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | Bulk request ID returned by Trove for later polling. |

## Native endpoint

Through the native Trove API, this operation is `POST /transactions/bulk` (base URL `https://trove.headline.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-bulk-transactions.md) for the provider-specific parameters and requirements.

