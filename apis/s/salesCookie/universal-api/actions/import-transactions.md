# Sales Cookie: Import Transactions

Imports transaction CSV data into Sales Cookie.

```
POST https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/import-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/import-transactions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionBatchId": "string",
  "csvContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/import-transactions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionBatchId": "string",
    "csvContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionBatchId` | string | yes | Batch ID returned by Prepare Full Transaction Import and sent in X-TransactionBatchId. |
| `csvContent` | string | yes | CSV content including the header row in the same order as the mapping XML. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sales Cookie API returns.

## Native endpoint

Through the native Sales Cookie API, this operation is `POST /Api/ImportData` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-transactions.md) for the provider-specific parameters and requirements.

