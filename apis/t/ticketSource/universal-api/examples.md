# TicketSource Universal API Examples

These examples use the MindCloud API key and TicketSource connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Retrieves events from the TicketSource account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-events?${params}`, {
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
      "attributes": {
        "activated": true,
        "archived": true,
        "category": "string",
        "comment": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "genre": "string",
        "images": [
          {
            "src": "string",
            "type": "string"
          }
        ],
        "keywords": "string",
        "name": "Ava Chen",
        "public": true,
        "reference": "string",
        "terms": "string",
        "thirdPartyConsent": {
          "capture": true,
          "name": "Ava Chen",
          "showConsent": {
            "email": true,
            "post": true,
            "sms": true
          }
        },
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "dates": "https://example.com",
        "self": "https://example.com",
        "venues": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketSource/latest/actions/list-events).

## Create Customer

Creates a new customer in TicketSource.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/create-customer', {
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
      "attributes": {
        "address": {
          "line1": "string",
          "line2": "string",
          "line3": "string",
          "line4": "string",
          "postcode": "string"
        },
        "consent": {
          "email": true,
          "post": true,
          "sms": true
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "membership": {
          "endDate": "2026-05-07T12:00:00.000Z",
          "identifier": "string",
          "startDate": "2026-05-07T12:00:00.000Z"
        },
        "phone": "string",
        "telephone": "string",
        "title": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "bookings": "https://example.com",
        "notes": "https://example.com",
        "self": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketSource/latest/actions/create-customer).
