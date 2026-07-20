# Zoho Meeting: Update Meeting

Updates an existing meeting in Zoho Meeting.

```
PUT https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/update-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/update-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "meetingKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/update-meeting', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "meetingKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |
| `meetingKey` | string | yes | Meeting key returned by List Meetings or Create Meeting. |
| `topic` | string | no | Meeting topic. |
| `startTime` | string | no | Meeting start time in Zoho's expected format. |
| `presenter` | string | no | Presenter user ID. |
| `duration` | number | no | Meeting duration. |
| `timezone` | string | no | Meeting timezone. |
| `agenda` | string | no | Meeting agenda or description. |
| `participants[]` | array<object> | no | Optional array of participant objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "session": {
        "accessCode": "string",
        "creator": "string",
        "creatorZuid": "string",
        "departmentId": "string",
        "departmentName": "Ava Chen",
        "dialinUrl": "https://example.com",
        "duration": "string",
        "encryptPassword": "string",
        "endTime": "string",
        "endTimeMillisec": 1,
        "isRecurring": true,
        "joinLink": "https://example.com",
        "meeting": {
          "zsoid": "string"
        },
        "meetingKey": "string",
        "offset": "string",
        "presenter": "string",
        "presenterEmail": "ava@example.com",
        "recurringType": "string",
        "registrationLink": "https://example.com",
        "shortenJoinUrl": "https://example.com",
        "source": "string",
        "startLink": "https://example.com",
        "startTime": "string",
        "startTimeMillisec": 1,
        "sys_id": 1,
        "timezone": "string",
        "topic": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `session.accessCode` | string |  |
| `session.creator` | string |  |
| `session.creatorZuid` | string |  |
| `session.departmentId` | string |  |
| `session.departmentName` | string |  |
| `session.dialinUrl` | string |  |
| `session.duration` | string |  |
| `session.encryptPassword` | string |  |
| `session.endTime` | string |  |
| `session.endTimeMillisec` | number |  |
| `session.isRecurring` | boolean |  |
| `session.joinLink` | string |  |
| `session.meeting.zsoid` | string |  |
| `session.meetingKey` | string |  |
| `session.offset` | string |  |
| `session.presenter` | string |  |
| `session.presenterEmail` | string |  |
| `session.recurringType` | string |  |
| `session.registrationLink` | string |  |
| `session.shortenJoinUrl` | string |  |
| `session.source` | string |  |
| `session.startLink` | string |  |
| `session.startTime` | string |  |
| `session.startTimeMillisec` | number |  |
| `session.sys_id` | number |  |
| `session.timezone` | string |  |
| `session.topic` | string |  |
| `session.type` | string |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `PUT /api/v2/:organizationId/sessions/:meetingKey.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-meeting.md) for the provider-specific parameters and requirements.

