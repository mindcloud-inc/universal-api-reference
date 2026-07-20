# HappyFox Universal API Examples

These examples use the MindCloud API key and HappyFox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tickets

Retrieves tickets from HappyFox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-tickets?${params}`, {
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
      "assignedTo": {},
      "attachmentsCount": 1,
      "category": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "displayId": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "firstMessage": "string",
      "id": 1,
      "lastStaffReplyAt": "2026-05-07T12:00:00.000Z",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "lastUserReplyAt": "2026-05-07T12:00:00.000Z",
      "messagesCount": 1,
      "priority": {},
      "slaBreaches": 1,
      "source": "string",
      "status": {},
      "subject": "string",
      "subscribers": [
        {}
      ],
      "tags": "string",
      "timeSpent": 1,
      "unresponded": true,
      "updates": [
        {}
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [List Tickets action reference](actions/list-tickets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/happyFox/latest/actions/list-tickets).

## Add Staff Private Note

Adds a private note to a ticket in HappyFox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/add-staff-private-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketNumber": "string",
  "staff": 1,
  "plainText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/add-staff-private-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketNumber": "string",
    "staff": 1,
    "plainText": "string"
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
      "assignedTo": {},
      "attachmentsCount": 1,
      "category": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "displayId": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "firstMessage": "string",
      "id": 1,
      "lastStaffReplyAt": "2026-05-07T12:00:00.000Z",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "lastUserReplyAt": "2026-05-07T12:00:00.000Z",
      "messagesCount": 1,
      "priority": {},
      "slaBreaches": 1,
      "source": "string",
      "status": {},
      "subject": "string",
      "subscribers": [
        {}
      ],
      "tags": "string",
      "timeSpent": 1,
      "unresponded": true,
      "updates": [
        {}
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Staff Private Note action reference](actions/add-staff-private-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/happyFox/latest/actions/add-staff-private-note).
