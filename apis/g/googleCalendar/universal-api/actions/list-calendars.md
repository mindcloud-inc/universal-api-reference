# Google Calendar: List Calendars

Retrieves calendar list entries from Google Calendar.

```
GET https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Calendar `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-calendars?${params}`, {
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
| `accessRole` | list | no |  |
| `showHidden` | boolean | no |  |
| `showDeleted` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessRole": "string",
      "backgroundColor": "string",
      "colorId": "string",
      "conferenceProperties": {
        "allowedConferenceSolutionTypes": [
          "string"
        ]
      },
      "defaultReminders": [
        {
          "method": "string",
          "minutes": 1
        }
      ],
      "etag": "string",
      "foregroundColor": "string",
      "id": "string",
      "kind": "string",
      "notificationSettings": {
        "notifications": [
          {
            "method": "string",
            "type": "string"
          }
        ]
      },
      "primary": true,
      "selected": true,
      "summary": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessRole` | string |  |
| `backgroundColor` | string |  |
| `colorId` | string |  |
| `conferenceProperties.allowedConferenceSolutionTypes[]` | string |  |
| `defaultReminders[].method` | string |  |
| `defaultReminders[].minutes` | number |  |
| `etag` | string |  |
| `foregroundColor` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `notificationSettings.notifications[].method` | string |  |
| `notificationSettings.notifications[].type` | string |  |
| `primary` | boolean |  |
| `selected` | boolean |  |
| `summary` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Google Calendar API, this operation is `GET users/me/calendarList` (base URL `https://www.googleapis.com/calendar/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

