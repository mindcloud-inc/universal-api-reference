# Teachlr Organizations: Create Meeting



```
POST https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/create-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps@mindcloud.co",
  "topic": "MindCloud Test Meeting",
  "date": "2026-04-03",
  "time": "10:00",
  "duration": "30",
  "timezone": "America/Sao_Paulo"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps@mindcloud.co",
    "topic": "MindCloud Test Meeting",
    "date": "2026-04-03",
    "time": "10:00",
    "duration": "30",
    "timezone": "America/Sao_Paulo"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email of the user who will host the meeting. Default: `apps@mindcloud.co`. |
| `topic` | string | yes | Topic of the meeting. Default: `MindCloud Test Meeting`. |
| `date` | string | yes | Meeting date in YYYY-MM-DD format. Default: `2026-04-03`. |
| `time` | string | yes | Meeting start time. Default: `10:00`. |
| `duration` | number | yes | Meeting duration in minutes. Default: `30`. |
| `timezone` | string | yes | Timezone identifier for the meeting. Default: `America/Sao_Paulo`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "duration": 1,
      "hostEmail": "ava@example.com",
      "meetingId": 1,
      "time": "string",
      "timezone": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `duration` | number |  |
| `hostEmail` | string |  |
| `meetingId` | number |  |
| `time` | string |  |
| `timezone` | string |  |
| `topic` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `POST /meetings` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meeting.md) for the provider-specific parameters and requirements.

