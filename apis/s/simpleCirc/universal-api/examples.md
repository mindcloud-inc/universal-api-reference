# SimpleCirc Universal API Examples

These examples use the MindCloud API key and SimpleCirc connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Subscribers

Retrieves a list of subscribers from SimpleCirc.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/list-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/list-subscribers?${params}`, {
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
      "subscribers": [
        {
          "account_id": "string",
          "address": {
            "address_1": "string",
            "address_2": "string",
            "city": "string",
            "country": "string",
            "state": "string",
            "zipcode": "string"
          },
          "company": "string",
          "custom_fields": {},
          "email": "ava@example.com",
          "first_name": "Ava",
          "last_name": "Chen",
          "login_link": "https://example.com",
          "name": "Ava Chen",
          "phone": "string",
          "renewal_link": "https://example.com",
          "subscriptions": [
            {
              "auto_renew": 1,
              "copies": 1,
              "digital_status": "string",
              "expiration_date": "string",
              "giftgiver": {},
              "issues_remaining": 1,
              "last_issue": 1,
              "last_order": {
                "amount_due": "string",
                "amount_paid": "string",
                "copies": 1,
                "custom_source": "string",
                "issues": "string",
                "never_expires": 1,
                "order_date_time": "string",
                "order_id": 1,
                "postage_type_id": 1,
                "price_description": "string",
                "promo_code": "string",
                "tax": "string"
              },
              "last_publish_date": "string",
              "last_volume": 1,
              "never_expires": 1,
              "postage_type_id": 1,
              "promo_code": "string",
              "publication_id": 1,
              "publication_name": "Ava Chen",
              "qualified": 1,
              "qualified_on": "string",
              "questions": {},
              "status": "string",
              "subscription_id": 1
            }
          ],
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Subscribers action reference](actions/list-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleCirc/latest/actions/list-subscribers).

## Create or Update Address

Creates or updates a subscriber address in SimpleCirc.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-or-update-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "address1": "string",
  "city": "string",
  "state": "string",
  "zipcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/create-or-update-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "address1": "string",
    "city": "string",
    "state": "string",
    "zipcode": "string"
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
      "subscriber": {
        "account_id": "string",
        "address": {
          "address_1": "string",
          "address_2": "string",
          "city": "string",
          "country": "string",
          "state": "string",
          "zipcode": "string"
        },
        "company": "string",
        "custom_fields": {},
        "email": "ava@example.com",
        "first_name": "Ava",
        "last_name": "Chen",
        "login_link": "https://example.com",
        "name": "Ava Chen",
        "phone": "string",
        "renewal_link": "https://example.com",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create or Update Address action reference](actions/create-or-update-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleCirc/latest/actions/create-or-update-address).
