# Zoho Meeting: Create Meeting

Creates a new meeting in Zoho Meeting.

```
POST https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "topic": "string",
  "startTime": "string",
  "presenter": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "topic": "string",
    "startTime": "string",
    "presenter": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |
| `topic` | string | yes | Meeting topic. |
| `startTime` | string | yes | Meeting start time in Zoho's expected format. |
| `presenter` | string | yes | Presenter user ID. |
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
        "departmentId": "string",
        "departmentName": "Ava Chen",
        "dialinUrl": "https://example.com",
        "duration": 1,
        "endTime": "string",
        "isRecurring": true,
        "joinLink": "https://example.com",
        "meeting": {
          "zsoid": "string"
        },
        "meetingKey": "string",
        "presenter": 1,
        "presenterEmail": "ava@example.com",
        "registrationLink": "https://example.com",
        "startLink": "https://example.com",
        "startTime": "string",
        "sys_id": "string",
        "timezone": "string",
        "topic": "string"
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
| `session.departmentId` | string |  |
| `session.departmentName` | string |  |
| `session.dialinUrl` | string |  |
| `session.duration` | number |  |
| `session.endTime` | string |  |
| `session.isRecurring` | boolean |  |
| `session.joinLink` | string |  |
| `session.meeting.zsoid` | string |  |
| `session.meetingKey` | string |  |
| `session.presenter` | number |  |
| `session.presenterEmail` | string |  |
| `session.registrationLink` | string |  |
| `session.startLink` | string |  |
| `session.startTime` | string |  |
| `session.sys_id` | string |  |
| `session.timezone` | string |  |
| `session.topic` | string |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `POST /api/v2/:organizationId/sessions.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meeting.md) for the provider-specific parameters and requirements.

