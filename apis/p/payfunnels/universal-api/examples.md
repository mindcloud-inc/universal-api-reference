# Payfunnels Universal API Examples

These examples use the MindCloud API key and Payfunnels connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Payments

Retrieves a list of payments from Payfunnels.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-payments?${params}`, {
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
      "billingAddress": {},
      "cardLast4": "string",
      "coupon": {},
      "createdAt": "string",
      "currencyCode": "string",
      "customer": {},
      "description": "string",
      "id": "string",
      "metadata": {},
      "processingFeeAmount": 1,
      "products": [
        {}
      ],
      "quantity": 1,
      "refundAmount": 1,
      "setupFeeAmount": 1,
      "shippingAddress": {},
      "status": "string",
      "taxAmount": 1,
      "title": "string",
      "totalAmountPaid": 1
    }
  ],
  "meta": {}
}
```

See the full [List Payments action reference](actions/list-payments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payfunnels/latest/actions/list-payments).

## Cancel Subscription

Updates a subscription by cancelling it in Payfunnels.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cancellationOption": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cancellationOption": "string",
    "id": "string"
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
      "chargeAmount": 1,
      "createdAt": "string",
      "customer": {},
      "endDate": "string",
      "id": "string",
      "metadata": {},
      "paymentMethod": {},
      "paymentType": "string",
      "startDate": "string",
      "status": "string",
      "title": "string",
      "totalCollectedAmount": 1,
      "totalDueAmount": 1,
      "totalMaxPayment": 1,
      "totalSubscriptionAmount": 1
    }
  ],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payfunnels/latest/actions/cancel-subscription).
