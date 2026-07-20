# Syncro Universal API Examples

These examples use the MindCloud API key and Syncro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact

Retrieves a contact from Syncro by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-contact?${params}`, {
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
      "accountId": 1,
      "address1": "string",
      "city": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "optOut": true,
      "phone": "string",
      "processedPhone": "string",
      "sinceUpdatedAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/syncro/latest/actions/get-contact).

## Add Ticket Comment

Adds a comment to a ticket in Syncro.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "subject": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "subject": "string",
    "body": "string"
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
      "comment": {
        "body": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "hidden": true,
        "id": 1,
        "subject": "string",
        "tech": "string",
        "ticketId": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userId": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Ticket Comment action reference](actions/add-ticket-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/syncro/latest/actions/add-ticket-comment).
