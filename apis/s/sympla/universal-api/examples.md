# Sympla Universal API Examples

These examples use the MindCloud API key and Sympla connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Retrieves the organizer's events from Sympla.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-events?${params}`, {
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
      "data": [
        {}
      ],
      "pagination": {},
      "sort": {}
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sympla/latest/actions/list-events).

## Check In Participant

Checks in a participant in Sympla by participant ID.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sympla/latest/actions/check-in-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "participantId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sympla/latest/actions/check-in-participant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "participantId": 1
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Check In Participant action reference](actions/check-in-participant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sympla/latest/actions/check-in-participant).
