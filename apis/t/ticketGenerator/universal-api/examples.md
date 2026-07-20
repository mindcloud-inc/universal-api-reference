# Ticket Generator Universal API Examples

These examples use the MindCloud API key and Ticket Generator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Event Details

Retrieves active event details and ticket categories from Ticket Generator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/get-event-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/get-event-details?${params}`, {
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
      "description": "string",
      "endDateTime": "string",
      "eventId": "string",
      "eventName": "Ava Chen",
      "eventType": "string",
      "note": "string",
      "seatsIoVenueData": {},
      "startDateTime": "string",
      "ticketCategories": [
        {}
      ],
      "timezone": "string",
      "venue": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Event Details action reference](actions/get-event-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketGenerator/latest/actions/get-event-details).

## Create Ticket QR Data

Creates ticket QR code data and ticket ID in Ticket Generator.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/create-ticket-qr-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "width": "300"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/create-ticket-qr-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "width": "300"
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
      "base64EncodedUrl": "https://example.com",
      "ticketCategoryName": "Ava Chen",
      "ticketId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Ticket QR Data action reference](actions/create-ticket-qr-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketGenerator/latest/actions/create-ticket-qr-data).
