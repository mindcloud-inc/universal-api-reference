# OnceHub Universal API Examples

These examples use the MindCloud API key and OnceHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/validate-api-key?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key action reference](actions/validate-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onceHub/latest/actions/validate-api-key).

## Cancel Booking



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/cancel-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/cancel-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "attendees": [
        "string"
      ],
      "bookingCalendar": "string",
      "bookingPage": {},
      "cancelRescheduleInformation": {
        "actionedBy": "string",
        "reason": "string",
        "userId": "string"
      },
      "cancelUrl": "https://example.com",
      "contact": "string",
      "conversation": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "customerTimezone": "string",
      "durationMinutes": 1,
      "eventType": {},
      "externalCalendar": {
        "eventId": {},
        "id": {},
        "name": {},
        "type": "string"
      },
      "formSubmission": {},
      "icsUrl": "https://example.com",
      "id": "string",
      "inTrash": true,
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "locationDescription": {},
      "masterPage": {},
      "object": "string",
      "owner": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "object": "string",
        "roleName": "Ava Chen",
        "status": "string",
        "teams": [
          "string"
        ],
        "timezone": "string"
      },
      "paymentInformation": {},
      "rescheduledBookingId": {},
      "rescheduleUrl": "https://example.com",
      "startingTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "trackingId": "string",
      "utmParams": {},
      "virtualConferencing": {}
    }
  ],
  "meta": {}
}
```

See the full [Cancel Booking action reference](actions/cancel-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onceHub/latest/actions/cancel-booking).
