# Cratejoy Universal API Examples

These examples use the MindCloud API key and Cratejoy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Cratejoy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-customers?${params}`, {
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
      "country": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "name": "Ava Chen",
      "num_orders": 1,
      "num_subscriptions": 1,
      "subscription_status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cratejoy/latest/actions/list-customers).

## Cancel Subscription

Cancels a subscription in Cratejoy.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": 1
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
      "autorenew": true,
      "credit": 1,
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "product_billing_id": 1,
      "skipped_date": "2026-05-07T12:00:00.000Z",
      "start_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cratejoy/latest/actions/cancel-subscription).
