# Zoho Calendar: Create Calendar

Creates a new personal calendar in Zoho Calendar.

```
POST https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-calendar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendarData` | object | yes | Calendar payload object describing the calendar to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendars": [
        {
          "caltype": "string",
          "category": "string",
          "color": "string",
          "description": "string",
          "id": "string",
          "include_infreebusy": true,
          "name": "Ava Chen",
          "status": true,
          "textcolor": "string",
          "timezone": "string",
          "uid": "string"
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
| `calendars[].caltype` | string |  |
| `calendars[].category` | string |  |
| `calendars[].color` | string |  |
| `calendars[].description` | string |  |
| `calendars[].id` | string |  |
| `calendars[].include_infreebusy` | boolean |  |
| `calendars[].name` | string |  |
| `calendars[].status` | boolean |  |
| `calendars[].textcolor` | string |  |
| `calendars[].timezone` | string |  |
| `calendars[].uid` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `POST /calendars` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar.md) for the provider-specific parameters and requirements.

