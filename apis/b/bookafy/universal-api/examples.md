# Bookafy Universal API Examples

These examples use the MindCloud API key and Bookafy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Staff Users

Retrieves staff users from Bookafy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-staff-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-staff-users?${params}`, {
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
      "email": "ava@example.com",
      "id": 1,
      "imageUrl": {},
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Staff Users action reference](actions/list-staff-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookafy/latest/actions/list-staff-users).

## Create Appointment

Creates an appointment in Bookafy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "response": {
        "appointment": {
          "appointmentDate": "2026-05-07T12:00:00.000Z",
          "appointmentEndTime": "2026-05-07T12:00:00.000Z",
          "appointmentStartTime": "2026-05-07T12:00:00.000Z",
          "cancelToken": "string",
          "category": {
            "categoryId": 1,
            "categoryName": "Ava Chen"
          },
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerId": 1,
          "description": "string",
          "duration": "string",
          "id": 1,
          "isActive": true,
          "service": {
            "serviceId": 1,
            "serviceName": "Ava Chen"
          },
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "updateToken": "string",
          "userId": 1
        },
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Appointment action reference](actions/create-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookafy/latest/actions/create-appointment).
