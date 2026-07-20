# Microsoft 365 Calendar: Create Event

Creates a new event in Microsoft 365 Calendar.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "MindCloud calendar test event",
  "start.dateTime": "2026-03-19T15:00:00",
  "end.dateTime": "2026-03-19T15:30:00"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "MindCloud calendar test event",
    "start.dateTime": "2026-03-19T15:00:00",
    "end.dateTime": "2026-03-19T15:30:00"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | The calendar event subject. Example: `MindCloud calendar test event`. |
| `start.dateTime` | string | yes | Event start date and time in ISO format. Use UTC values such as 2026-03-19T15:00:00. Example: `2026-03-19T15:00:00`. |
| `end.dateTime` | string | yes | Event end date and time in ISO format. Use UTC values such as 2026-03-19T15:30:00. Example: `2026-03-19T15:30:00`. |
| `location.displayName` | string | no | Optional event location display name. Example: `MindCloud HQ`. |

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

Through the native Microsoft 365 Calendar API, this operation is `POST /v1.0/me/events` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

