# Let's Calendar: Schedule Calendar Invites

Schedules calendar invites in Let's Calendar.

```
POST https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/schedule-calendar-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/schedule-calendar-invites" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "scheduleDate": "string",
  "scheduleTime": "string",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/schedule-calendar-invites', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "scheduleDate": "string",
    "scheduleTime": "string",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The unique identifier of the campaign. |
| `scheduleDate` | string | yes | The date for scheduling in Y-m-d format. |
| `scheduleTime` | string | yes | The time for scheduling in H:i format. |
| `timezone` | string | yes | The timezone for the schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "scheduledTime": "string",
      "scheduleId": 1,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `scheduledTime` | string |  |
| `scheduleId` | number |  |
| `timezone` | string |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `POST schedule-invite` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-calendar-invites.md) for the provider-specific parameters and requirements.

