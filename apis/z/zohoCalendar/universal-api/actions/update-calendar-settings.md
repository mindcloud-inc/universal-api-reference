# Zoho Calendar: Update Calendar Settings

Updates calendar settings in Zoho Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/update-calendar-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/update-calendar-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "settingsData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/update-calendar-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "settingsData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `settingsData` | object | yes | Settings payload object with the calendar settings to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "settings": [
        {
          "message": "string",
          "preference": {
            "allow_eventinvite": "string",
            "allow_groupinvite": "string",
            "dateformat": "string",
            "default_view": "string",
            "display_deniedevents": true,
            "event_duration": "string",
            "fontsize": "string",
            "guest_perm": "string",
            "hourend": "string",
            "hourstart": "string",
            "nonworkinghours_busy": true,
            "theme": "string",
            "timeformat": 1,
            "timezone": "string",
            "weekstart": "string",
            "workweek_end": "string",
            "workweek_start": "string"
          },
          "status": "string"
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
| `settings[].message` | string |  |
| `settings[].preference.allow_eventinvite` | string |  |
| `settings[].preference.allow_groupinvite` | string |  |
| `settings[].preference.dateformat` | string |  |
| `settings[].preference.default_view` | string |  |
| `settings[].preference.display_deniedevents` | boolean |  |
| `settings[].preference.event_duration` | string |  |
| `settings[].preference.fontsize` | string |  |
| `settings[].preference.guest_perm` | string |  |
| `settings[].preference.hourend` | string |  |
| `settings[].preference.hourstart` | string |  |
| `settings[].preference.nonworkinghours_busy` | boolean |  |
| `settings[].preference.theme` | string |  |
| `settings[].preference.timeformat` | number |  |
| `settings[].preference.timezone` | string |  |
| `settings[].preference.weekstart` | string |  |
| `settings[].preference.workweek_end` | string |  |
| `settings[].preference.workweek_start` | string |  |
| `settings[].status` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `PUT /settings` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-calendar-settings.md) for the provider-specific parameters and requirements.

