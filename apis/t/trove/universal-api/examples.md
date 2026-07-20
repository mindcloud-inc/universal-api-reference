# Trove Universal API Examples

These examples use the MindCloud API key and Trove connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Enrich Sample Transaction

Retrieves enrichment details for a sample transaction from Trove.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-sample-transaction?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-sample-transaction?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Enrich Sample Transaction action reference](actions/enrich-sample-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trove/latest/actions/enrich-sample-transaction).

## Enrich Bulk Transactions

Creates a bulk transaction enrichment request in Trove.

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

Example response:

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

See the full [Enrich Bulk Transactions action reference](actions/enrich-bulk-transactions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trove/latest/actions/enrich-bulk-transactions).
