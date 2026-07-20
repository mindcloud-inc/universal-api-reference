# Pabbly Subscription Billing Universal API Examples

These examples use the MindCloud API key and Pabbly Subscription Billing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Customers



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-customers?${params}`, {
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
      "billingAddress": {
        "city": "string",
        "country": "string",
        "state": "string",
        "stateCode": "string",
        "street1": "string",
        "zipCode": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "shippingAddress": {
        "city": "string",
        "country": "string",
        "state": "string",
        "stateCode": "string",
        "street1": "string",
        "zipCode": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List All Customers action reference](actions/list-all-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pabblySubscriptionBilling/latest/actions/list-all-customers).

## Add Credit



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/add-credit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/add-credit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditNoteId": "string",
      "customerId": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "planId": "string",
      "productId": "string",
      "quantity": 1,
      "rate": 1,
      "remainingAmount": 1,
      "status": "string",
      "subscriptionId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "used": [
        "string"
      ],
      "usedDays": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Credit action reference](actions/add-credit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pabblySubscriptionBilling/latest/actions/add-credit).
