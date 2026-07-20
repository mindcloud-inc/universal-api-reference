# HelpSpace Universal API Examples

These examples use the MindCloud API key and HelpSpace connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tickets

Retrieves tickets from HelpSpace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-tickets?${params}`, {
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
      "assignee": {},
      "channel": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {},
      "customFields": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "fromContact": {},
      "id": 1,
      "lastContact": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "tags": [
        "string"
      ],
      "team": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Tickets action reference](actions/list-tickets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helpSpace/latest/actions/list-tickets).

## Create Customer

Creates a new customer in HelpSpace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-customer', {
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
      "address": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "email": "ava@example.com",
      "id": 1,
      "jobTitle": "string",
      "locale": "string",
      "name": "Ava Chen",
      "note": "string",
      "postalCode": "string",
      "state": "string",
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helpSpace/latest/actions/create-customer).
