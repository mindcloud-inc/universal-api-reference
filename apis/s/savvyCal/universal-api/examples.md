# SavvyCal Universal API Examples

These examples use the MindCloud API key and SavvyCal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/get-current-user?${params}`, {
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
      "avatarUrl": "https://example.com",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstDayOfWeek": 1,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "plan": "string",
      "timeFormat": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/savvyCal/latest/actions/get-current-user).

## Cancel Event



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/cancel-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/cancel-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string"
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
      "additionalInfo": "string",
      "attendees": [
        {
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": "string",
          "isOrganizer": true,
          "responseStatus": "string"
        }
      ],
      "bufferAfter": 1,
      "bufferBefore": 1,
      "conferencing": {
        "joinUrl": "https://example.com",
        "meetingId": "string",
        "type": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "endAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isGroupSession": true,
      "link": {
        "id": "https://example.com",
        "name": "https://example.com",
        "slug": "https://example.com"
      },
      "location": "string",
      "maximumGroupSize": 1,
      "organizer": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string"
      },
      "payment": {
        "amountTotal": 1,
        "state": "string"
      },
      "scheduler": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string"
      },
      "scope": {
        "id": "string",
        "name": "Ava Chen",
        "slug": "string"
      },
      "startAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "summary": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Event action reference](actions/cancel-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/savvyCal/latest/actions/cancel-event).
