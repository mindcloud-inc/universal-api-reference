# Microsoft 365 Calendar: Update Event

Updates an existing event in Microsoft 365 Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "AAMkAG..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The ID of the Outlook event to update. Example: `AAMkAG...`. |
| `subject` | string | no | Updated subject for the Outlook event. Example: `Updated MindCloud calendar test event`. |
| `start.dateTime` | string | no | Optional updated event start date and time. Example: `2026-04-14T15:00:00`. |
| `end.dateTime` | string | no | Optional updated event end date and time. Example: `2026-04-14T15:30:00`. |
| `location.displayName` | string | no | Optional updated event location display name. Example: `Conference Room`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start.timeZone` | string | no | Optional updated event start time zone. Provide this when changing the start date/time. Example: `UTC`. |
| `end.timeZone` | string | no | Optional updated event end time zone. Provide this when changing the end date/time. Example: `UTC`. |

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
| `bodyPreview` | string | Plain-text preview of the event body. |
| `end.dateTime` | string | Event end date and time. |
| `end.timeZone` | string | Event end time zone. |
| `id` | string | Event ID. |
| `isAllDay` | boolean | Whether the event lasts all day. |
| `isCancelled` | boolean | Whether the event is cancelled. |
| `location.displayName` | string | Event location display name. |
| `organizer.emailAddress.address` | string | Organizer email address. |
| `organizer.emailAddress.name` | string | Organizer display name. |
| `start.dateTime` | string | Event start date and time. |
| `start.timeZone` | string | Event start time zone. |
| `subject` | string | Event subject. |
| `webLink` | string | Outlook web URL for the event. |

## Native endpoint

Through the native Microsoft 365 Calendar API, this operation is `PATCH /v1.0/me/events/{{eventId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

