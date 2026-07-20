# Microsoft 365 Calendar: List Calendar View

Retrieves events from Microsoft 365 Calendar for a time range.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendar-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendar-view?connectionId=$CONNECTION_ID&startDateTime=2026-03-19T00%3A00%3A00Z&endDateTime=2026-03-20T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateTime": "2026-03-19T00:00:00Z",
  "endDateTime": "2026-03-20T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendar-view?${params}`, {
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
| `startDateTime` | string | yes | Start of the calendar view window in ISO 8601 format. Example: `2026-03-19T00:00:00Z`. |
| `endDateTime` | string | yes | End of the calendar view window in ISO 8601 format. Example: `2026-03-20T00:00:00Z`. |
| `top` | number | no | Number of events to return in the requested calendar window. Default: `10`. Example: `10`. |

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

Through the native Microsoft 365 Calendar API, this operation is `GET /v1.0/me/calendarView` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-view.md) for the provider-specific parameters and requirements.

