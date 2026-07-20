# Teachlr Organizations: Update Meeting



```
PUT https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/update-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/update-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/update-meeting', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | no | Updated meeting date. |
| `meetingId` | string | yes | Identifier of the meeting to update. |
| `time` | string | no | Updated meeting time. |
| `timezone` | string | no | Updated meeting timezone. |
| `topic` | string | no | Updated topic of the meeting. |
| `duration` | number | no | Updated meeting duration. |

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

Through the native Teachlr Organizations API, this operation is `PUT /meetings/:meetingId` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-meeting.md) for the provider-specific parameters and requirements.

