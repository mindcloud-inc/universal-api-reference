# Zoho Calendar: Get Calendar Settings

Retrieves calendar settings from Zoho Calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-calendar-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-calendar-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-calendar-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "settings": [
        {
          "agendanotify": "string",
          "allow_eventinvite": "string",
          "allow_groupinvite": "string",
          "dateformat": "string",
          "default_view": "string",
          "defEveCreationCal": "string",
          "display_deniedevents": true,
          "email": "ava@example.com",
          "emailformat": "ava@example.com",
          "event_duration": 1,
          "fontsize": "string",
          "guest_perm": 1,
          "hourend": 1,
          "hourstart": 1,
          "layout": 1,
          "listview": true,
          "new_version": 1,
          "nonworkinghours_busy": true,
          "notifyemail": "ava@example.com",
          "remindernotify": "string",
          "show_allevents": true,
          "show_weekno": true,
          "show_workhour": true,
          "theme": "string",
          "time_grid": 1,
          "timeformat": "string",
          "timezone": "string",
          "timezone_change": true,
          "weekstart": 1,
          "workweek_end": 1,
          "workweek_start": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `settings[].agendanotify` | string |  |
| `settings[].allow_eventinvite` | string |  |
| `settings[].allow_groupinvite` | string |  |
| `settings[].dateformat` | string |  |
| `settings[].default_view` | string |  |
| `settings[].defEveCreationCal` | string |  |
| `settings[].display_deniedevents` | boolean |  |
| `settings[].email` | string |  |
| `settings[].emailformat` | string |  |
| `settings[].event_duration` | number |  |
| `settings[].fontsize` | string |  |
| `settings[].guest_perm` | number |  |
| `settings[].hourend` | number |  |
| `settings[].hourstart` | number |  |
| `settings[].layout` | number |  |
| `settings[].listview` | boolean |  |
| `settings[].new_version` | number |  |
| `settings[].nonworkinghours_busy` | boolean |  |
| `settings[].notifyemail` | string |  |
| `settings[].remindernotify` | string |  |
| `settings[].show_allevents` | boolean |  |
| `settings[].show_weekno` | boolean |  |
| `settings[].show_workhour` | boolean |  |
| `settings[].theme` | string |  |
| `settings[].time_grid` | number |  |
| `settings[].timeformat` | string |  |
| `settings[].timezone` | string |  |
| `settings[].timezone_change` | boolean |  |
| `settings[].weekstart` | number |  |
| `settings[].workweek_end` | number |  |
| `settings[].workweek_start` | number |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /settings` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar-settings.md) for the provider-specific parameters and requirements.

