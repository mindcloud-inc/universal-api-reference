# Microsoft 365: List Calendar View

Retrieves calendar view events from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-calendar-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-calendar-view?connectionId=$CONNECTION_ID&startDateTime=2026-03-19T00%3A00%3A00Z&endDateTime=2026-03-20T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateTime": "2026-03-19T00:00:00Z",
  "endDateTime": "2026-03-20T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-calendar-view?${params}`, {
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

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/calendarView` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-view.md) for the provider-specific parameters and requirements.

