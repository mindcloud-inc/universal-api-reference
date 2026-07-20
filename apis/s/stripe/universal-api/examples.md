# Stripe Universal API Examples

These examples use the MindCloud API key and Stripe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from your Stripe account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-customers?${params}`, {
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
      "created": 1,
      "currency": "string",
      "delinquent": true,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stripe/latest/actions/list-customers).

## Cancel Payment Intent

Cancels an existing payment intent in Stripe.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/cancel-payment-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "intent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/cancel-payment-intent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "intent": "string"
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
      "amount": 1,
      "amountCapturable": 1,
      "amountReceived": 1,
      "canceledAt": 1,
      "cancellationReason": "string",
      "captureMethod": "string",
      "clientSecret": "string",
      "created": 1,
      "currency": "string",
      "description": "string",
      "id": "string",
      "latestCharge": "string",
      "object": "string",
      "paymentMethod": "string",
      "paymentMethodTypes": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Payment Intent action reference](actions/cancel-payment-intent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stripe/latest/actions/cancel-payment-intent).
