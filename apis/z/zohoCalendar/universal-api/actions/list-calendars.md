# Zoho Calendar: List Calendars

Retrieves user calendars from Zoho Calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-calendars?${params}`, {
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
| `category` | string | no | Filter calendars by category: own, group, app, others, or all. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendars": [
        {
          "alarm": [
            {
              "action": "string",
              "trigger": "string"
            }
          ],
          "calendar_createdtime": 1,
          "calendar_modifiedtime": 1,
          "caltype": "string",
          "canSendMail": true,
          "category": "string",
          "color": "string",
          "createdtime": 1,
          "ctag": 1,
          "description": "string",
          "id": "string",
          "include_infreebusy": true,
          "isdefault": true,
          "lastmodifiedtime": "2026-05-07T12:00:00.000Z",
          "modifiedtime": 1,
          "name": "Ava Chen",
          "order": 1,
          "owner": "string",
          "privilege": "string",
          "reminders": [
            {
              "action": "string",
              "minutes": "string"
            }
          ],
          "status": true,
          "textcolor": "string",
          "timezone": "string",
          "type": 1,
          "uid": "string",
          "visibility": true
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
| `calendars[].alarm[].action` | string |  |
| `calendars[].alarm[].trigger` | string |  |
| `calendars[].calendar_createdtime` | number |  |
| `calendars[].calendar_modifiedtime` | number |  |
| `calendars[].caltype` | string |  |
| `calendars[].canSendMail` | boolean |  |
| `calendars[].category` | string |  |
| `calendars[].color` | string |  |
| `calendars[].createdtime` | number |  |
| `calendars[].ctag` | number |  |
| `calendars[].description` | string |  |
| `calendars[].id` | string |  |
| `calendars[].include_infreebusy` | boolean |  |
| `calendars[].isdefault` | boolean |  |
| `calendars[].lastmodifiedtime` | date |  |
| `calendars[].modifiedtime` | number |  |
| `calendars[].name` | string |  |
| `calendars[].order` | number |  |
| `calendars[].owner` | string |  |
| `calendars[].privilege` | string |  |
| `calendars[].reminders[].action` | string |  |
| `calendars[].reminders[].minutes` | string |  |
| `calendars[].status` | boolean |  |
| `calendars[].textcolor` | string |  |
| `calendars[].timezone` | string |  |
| `calendars[].type` | number |  |
| `calendars[].uid` | string |  |
| `calendars[].visibility` | boolean |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /calendars` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

