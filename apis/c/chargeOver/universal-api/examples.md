# ChargeOver Universal API Examples

These examples use the MindCloud API key and ChargeOver connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customer account records from ChargeOver.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-customers?${params}`, {
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
      "arr": 1,
      "balance": 1,
      "company": "string",
      "customer_id": 1,
      "customer_status_name": "Ava Chen",
      "display_as": "string",
      "mrr": 1,
      "paid": 1,
      "superuser_email": "ava@example.com",
      "superuser_name": "Ava Chen",
      "total": 1,
      "url_self": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeOver/latest/actions/list-customers).

## Cancel Subscription

Cancels an existing subscription in ChargeOver.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": 1
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
      "value": true
    }
  ],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeOver/latest/actions/cancel-subscription).
