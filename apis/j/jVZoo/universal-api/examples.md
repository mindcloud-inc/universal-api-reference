# JVZoo Universal API Examples

These examples use the MindCloud API key and JVZoo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Latest Transactions

Retrieves latest transactions across your JVZoo products.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-latest-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-latest-transactions?${params}`, {
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
      "affiliateId": 1,
      "affiliateName": "Ava Chen",
      "customerEmail": "ava@example.com",
      "date": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "ip": "string",
      "lastName": "Chen",
      "price": "string",
      "productId": 1,
      "productName": "Ava Chen",
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Latest Transactions action reference](actions/get-latest-transactions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jVZoo/latest/actions/get-latest-transactions).

## Cancel Recurring Payment

Cancels a recurring payment in JVZoo.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/cancel-recurring-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "preKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/cancel-recurring-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "preKey": "string"
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
      "canceled": true
    }
  ],
  "meta": {}
}
```

See the full [Cancel Recurring Payment action reference](actions/cancel-recurring-payment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jVZoo/latest/actions/cancel-recurring-payment).
