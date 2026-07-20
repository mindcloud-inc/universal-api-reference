# Zoho Assist: Schedule Session

Schedules a remote support or screen sharing session in Zoho Assist.

```
POST https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/schedule-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/schedule-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "customerEmail": "ava@example.com",
  "scheduleTime": 1,
  "scheduleUpTo": 1,
  "utcOffset": "string",
  "timeZone": "string",
  "reminder": "0",
  "departmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/schedule-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "customerEmail": "ava@example.com",
    "scheduleTime": 1,
    "scheduleUpTo": 1,
    "utcOffset": "string",
    "timeZone": "string",
    "reminder": "0",
    "departmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title of the scheduled session. |
| `notes` | string | no | Description or notes for the scheduled session. |
| `customerEmail` | string | yes | Email address to invite to the scheduled session. |
| `scheduleTime` | number | yes | Scheduled start time in Unix milliseconds. |
| `scheduleUpTo` | number | yes | Estimated session end time in Unix milliseconds. |
| `utcOffset` | string | yes | UTC offset for the scheduled time zone. |
| `timeZone` | string | yes | IANA time zone for the scheduled session. |
| `reminder` | number | yes | Reminder offset for the scheduled session. Default: `0`. |
| `departmentId` | string | yes | Department in which the session should be scheduled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerUrl": "https://example.com",
      "scheduleId": "string",
      "statue": "string",
      "technicianUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerUrl` | string |  |
| `scheduleId` | string |  |
| `statue` | string |  |
| `technicianUrl` | string |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `POST /session/schedule` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-session.md) for the provider-specific parameters and requirements.

