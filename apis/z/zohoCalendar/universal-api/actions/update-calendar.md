# Zoho Calendar: Update Calendar

Updates an existing calendar in Zoho Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/update-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/update-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarUid": "string",
  "calendarData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/update-calendar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarUid": "string",
    "calendarData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendarUid` | string | yes | Calendar unique identifier. |
| `calendarData` | object | yes | Calendar payload object with the fields to update. |

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

Through the native Zoho Calendar API, this operation is `PUT /calendars/:calendaruid` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-calendar.md) for the provider-specific parameters and requirements.

