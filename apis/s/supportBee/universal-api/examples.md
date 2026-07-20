# SupportBee Universal API Examples

These examples use the MindCloud API key and SupportBee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tickets

Retrieves tickets from SupportBee.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-tickets?${params}`, {
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
      "currentPage": 1,
      "perPage": 1,
      "tickets": [
        [
          {}
        ]
      ],
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

See the full [List Tickets action reference](actions/list-tickets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/supportBee/latest/actions/list-tickets).

## Add Label to Ticket

Adds a label to a SupportBee ticket.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/add-label-to-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1,
  "labelName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/add-label-to-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": 1,
    "labelName": "Ava Chen"
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
      "label": {
        "id": 1,
        "label": "string",
        "ticket": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Label to Ticket action reference](actions/add-label-to-ticket.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/supportBee/latest/actions/add-label-to-ticket).
