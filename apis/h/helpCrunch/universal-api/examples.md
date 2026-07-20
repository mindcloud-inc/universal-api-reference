# HelpCrunch Universal API Examples

These examples use the MindCloud API key and HelpCrunch connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves a list of customers from HelpCrunch.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-customers?${params}`, {
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
      "blocked": true,
      "company": "string",
      "createdFrom": "string",
      "customData": [
        {}
      ],
      "device": {},
      "email": "ava@example.com",
      "firstSeen": "string",
      "id": 1,
      "integrationId": "string",
      "lastPage": "string",
      "lastSeen": "string",
      "locale": "string",
      "location": {},
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "referer": "string",
      "source": "string",
      "tags": [
        {}
      ],
      "unsubscribed": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helpCrunch/latest/actions/list-customers).

## Add Customer Event

Creates a new customer event in HelpCrunch.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/add-customer-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/add-customer-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": 1,
    "name": "Ava Chen"
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
      "data": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Customer Event action reference](actions/add-customer-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helpCrunch/latest/actions/add-customer-event).
