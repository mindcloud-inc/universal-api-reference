# Saastic Universal API Examples

These examples use the MindCloud API key and Saastic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Saastic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customers?${params}`, {
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
      "charges_count": 1,
      "charges_sum": 1,
      "city": "string",
      "company": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "has_subscription": 1,
      "id": 1,
      "last_name": "Chen",
      "location_id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "review_link": "https://example.com",
      "state": "string",
      "updated_at": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/saastic/latest/actions/list-customers).

## Create Customer Charge

Creates a customer charge in Saastic.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-customer-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/saastic/latest/actions/create-customer-charge', {
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
      "charged_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer Charge action reference](actions/create-customer-charge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/saastic/latest/actions/create-customer-charge).
