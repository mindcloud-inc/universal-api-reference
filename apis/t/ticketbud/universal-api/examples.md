# Ticketbud Universal API Examples

These examples use the MindCloud API key and Ticketbud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Ticketbud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-current-user?${params}`, {
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
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketbud/latest/actions/get-current-user).

## Check In Ticket

Checks in a ticket in Ticketbud.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/check-in-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/check-in-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
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
      "meta": {},
      "ticket": {}
    }
  ],
  "meta": {}
}
```

See the full [Check In Ticket action reference](actions/check-in-ticket.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketbud/latest/actions/check-in-ticket).
