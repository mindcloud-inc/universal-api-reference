# Google Calendar: Get Calendar List Entry

Retrieves a calendar list entry from Google Calendar.

```
GET https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/get-calendar-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/get-calendar-list-entry?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/get-calendar-list-entry?${params}`, {
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
| `calendar` | list | no |  |

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

Through the native Google Calendar API, this operation is `GET users/me/calendarList/:calendar` (base URL `https://www.googleapis.com/calendar/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar-list-entry.md) for the provider-specific parameters and requirements.

