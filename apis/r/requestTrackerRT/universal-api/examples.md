# Request Tracker (RT) Universal API Examples

These examples use the MindCloud API key and Request Tracker (RT) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Queues

Retrieves queues from Request Tracker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/list-queues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/list-queues?${params}`, {
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
      "id": "string",
      "type": "string",
      "Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Queues action reference](actions/list-queues.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/requestTrackerRT/latest/actions/list-queues).

## Comment on Ticket

Adds a comment to a ticket in Request Tracker.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/comment-on-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "contentType": "text/plain",
  "ticketId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/comment-on-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "contentType": "text/plain",
    "ticketId": "string"
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

See the full [Comment on Ticket action reference](actions/comment-on-ticket.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/requestTrackerRT/latest/actions/comment-on-ticket).
