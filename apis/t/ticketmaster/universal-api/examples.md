# Ticketmaster Universal API Examples

These examples use the MindCloud API key and Ticketmaster connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Finds events in Ticketmaster by location, date, and availability.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-events?${params}`, {
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
      "classifications": [
        {}
      ],
      "dates": {},
      "id": "string",
      "images": [
        {}
      ],
      "info": "string",
      "locale": "string",
      "location": {},
      "name": "Ava Chen",
      "pleaseNote": "string",
      "seatmap": {},
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketmaster/latest/actions/list-events).
