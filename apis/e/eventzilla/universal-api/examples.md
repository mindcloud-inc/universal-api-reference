# Eventzilla Universal API Examples

These examples use the MindCloud API key and Eventzilla connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Retrieves events from Eventzilla.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-events?${params}`, {
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
      "bgimageUrl": "https://example.com",
      "categories": "string",
      "currency": "string",
      "dateid": 1,
      "description": "string",
      "descriptionHtml": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "endTime": "string",
      "id": 1,
      "inviteCode": "string",
      "language": "string",
      "logoUrl": "https://example.com",
      "showRemaining": true,
      "startDate": "2026-05-07T12:00:00.000Z",
      "startTime": "string",
      "status": "string",
      "ticketsSold": 1,
      "ticketsTotal": 1,
      "timeZone": "string",
      "timezoneCode": "string",
      "title": "string",
      "twitterHashtag": "string",
      "url": "https://example.com",
      "utcOffset": "string",
      "venue": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventzilla/latest/actions/list-events).

## Cancel Event Order

Cancels an event order in Eventzilla.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/cancel-event-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkoutId": 1,
  "eventId": 1,
  "comments": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/cancel-event-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkoutId": 1,
    "eventId": 1,
    "comments": "string"
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
      "ordercancel": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Event Order action reference](actions/cancel-event-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventzilla/latest/actions/cancel-event-order).
