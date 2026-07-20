# More Good Reviews Universal API Examples

These examples use the MindCloud API key and More Good Reviews connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from More Good Reviews.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customers?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "charges_avg": 1,
      "charges_count": 1,
      "charges_sum": 1,
      "city": "string",
      "color": "string",
      "company": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "first_asked_at": 1,
      "first_charged_at": 1,
      "first_name": "Ava",
      "gravatar": "string",
      "has_subscription": 1,
      "id": 1,
      "is_validated": true,
      "lang": "string",
      "last_asked_at": 1,
      "last_charged_at": 1,
      "last_name": "Chen",
      "location_id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "phone_e164": "string",
      "phone_formatted": "string",
      "postal_code": "string",
      "review_link": "https://example.com",
      "signed_up_at": 1,
      "state": "string",
      "unsubscribe_link": "https://example.com",
      "updated_at": 1,
      "uuid": "string",
      "validation": {
        "address": "string",
        "engagement": {
          "engaging": true,
          "is_bot": true
        },
        "is_disposable_address": true,
        "is_role_address": true,
        "reason": [
          "string"
        ],
        "result": "string",
        "risk": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moreGoodReviews/latest/actions/list-customers).

## Create Customer Charge

Creates a customer charge in More Good Reviews.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/create-customer-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/create-customer-charge', {
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

See the full [Create Customer Charge action reference](actions/create-customer-charge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moreGoodReviews/latest/actions/create-customer-charge).
