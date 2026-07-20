# Paystack Universal API Examples

These examples use the MindCloud API key and Paystack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Transactions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-transactions?${params}`, {
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
      "amount": 1,
      "authorization": {},
      "channel": "string",
      "created_at": "string",
      "currency": "string",
      "customer": {},
      "gateway_response": "string",
      "id": 1,
      "paid_at": "string",
      "reference": "string",
      "requested_amount": 1,
      "status": "string",
      "transaction_date": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Transactions action reference](actions/list-transactions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paystack/latest/actions/list-transactions).

## Create Customer



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "createdAt": "string",
      "customer_code": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "identified": true,
      "last_name": "Chen",
      "metadata": {},
      "phone": "string",
      "risk_action": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paystack/latest/actions/create-customer).
