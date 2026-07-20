# GrooveHQ Universal API Examples

These examples use the MindCloud API key and GrooveHQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from GrooveHQ.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lastSignInAt": "2026-05-07T12:00:00.000Z",
      "links": {},
      "preferredMailboxId": "string",
      "role": "string",
      "state": "string",
      "subdomain": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grooveHQ/latest/actions/get-current-user).

## Add Ticket Labels

Adds labels to a ticket in GrooveHQ.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/add-ticket-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketNumber": "1001",
  "tags[]": "vip, urgent"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/add-ticket-labels', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketNumber": "1001",
    "tags[]": "vip, urgent"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Ticket Labels action reference](actions/add-ticket-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grooveHQ/latest/actions/add-ticket-labels).
