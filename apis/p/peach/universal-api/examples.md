# Peach Universal API Examples

These examples use the MindCloud API key and Peach connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Transactions

Retrieves transaction records from Peach.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peach/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peach/latest/actions/list-transactions?${params}`, {
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
  "data": [
    {
      "paginationKey": {
        "accountId": "string",
        "transactionDate": 1,
        "transactionId": "string"
      },
      "results": [
        {
          "amount": 1,
          "campaignId": "string",
          "category": "string",
          "contactId": "string",
          "currency": "string",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "firstName": "Ava",
          "isCancelled": true,
          "isCompleted": true,
          "lastName": "Chen",
          "paymentMethod": "string",
          "paymentType": "string",
          "receiptNumber": 1,
          "receiptUrl": "https://example.com",
          "status": "string",
          "sum": 1,
          "transactionDate": "2026-05-07T12:00:00.000Z",
          "transactionId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Transactions action reference](actions/list-transactions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peach/latest/actions/list-transactions).

## Cancel Subscription

Updates a subscription payment in Peach by canceling it.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/peach/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peach/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentId": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peach/latest/actions/cancel-subscription).
