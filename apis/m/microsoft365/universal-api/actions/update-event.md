# Microsoft 365: Update Event

Updates an event in Microsoft 365.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "AQMkADAwATNi..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "AQMkADAwATNi..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The ID of the Outlook event to update. Example: `AQMkADAwATNi...`. |
| `subject` | string | no | Updated subject for the Outlook event. Example: `Updated MindCloud calendar test event`. |
| `start.dateTime` | string | no | Updated event start date and time in ISO format. Provide this with an updated end date and time. Example: `2026-03-19T16:00:00`. |
| `end.dateTime` | string | no | Updated event end date and time in ISO format. Provide this with an updated start date and time. Example: `2026-03-19T16:30:00`. |
| `start.timeZone` | string | no | Time zone to use with the updated event start date and time. Example: `UTC`. |
| `end.timeZone` | string | no | Time zone to use with the updated event end date and time. Example: `UTC`. |
| `location.displayName` | string | no | Updated display name for the event location. Example: `Updated MindCloud test meeting room`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyPreview": "string",
      "end": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "id": "string",
      "isAllDay": true,
      "isCancelled": true,
      "location": {
        "displayName": "Ava Chen"
      },
      "organizer": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "start": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "subject": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyPreview` | string |  |
| `end.dateTime` | string |  |
| `end.timeZone` | string |  |
| `id` | string |  |
| `isAllDay` | boolean |  |
| `isCancelled` | boolean |  |
| `location.displayName` | string |  |
| `organizer.emailAddress.address` | string |  |
| `organizer.emailAddress.name` | string |  |
| `start.dateTime` | string |  |
| `start.timeZone` | string |  |
| `subject` | string |  |
| `webLink` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `PATCH /v1.0/me/events/{{eventId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

