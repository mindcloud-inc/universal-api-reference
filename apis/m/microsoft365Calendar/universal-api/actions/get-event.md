# Microsoft 365 Calendar: Get Event

Retrieves an event from Microsoft 365 Calendar.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/get-event?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The ID of the Outlook event. Example: `AAMkAG...`. |

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

Through the native Microsoft 365 Calendar API, this operation is `GET /v1.0/me/events/{{eventId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

