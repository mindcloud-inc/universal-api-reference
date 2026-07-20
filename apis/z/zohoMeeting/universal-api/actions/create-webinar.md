# Zoho Meeting: Create Webinar

Creates a new webinar in Zoho Meeting.

```
POST https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-webinar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-webinar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "topic": "string",
  "startTime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/create-webinar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "topic": "string",
    "startTime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |
| `topic` | string | yes | Webinar topic. |
| `startTime` | string | yes | Webinar start time in Zoho's expected format. |
| `duration` | number | no | Webinar duration. |
| `timezone` | string | no | Webinar timezone. |
| `agenda` | string | no | Webinar agenda or description. |
| `presenter` | string | no | Presenter user ID. |
| `participants[]` | array<object> | no | Optional array of participant objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "session": {
        "creatorZuid": "string",
        "departmentId": "string",
        "departmentName": "Ava Chen",
        "duration": 1,
        "endTime": "string",
        "endTimeMillisec": 1,
        "isDepartmentAdmin": true,
        "meeting": {
          "zsoid": "string"
        },
        "meetingKey": "string",
        "offset": "string",
        "presenter": 1,
        "presenterEmail": "ava@example.com",
        "recurringType": 1,
        "regEmbedURL": "https://example.com",
        "registrationLink": "https://example.com",
        "sessionType": "string",
        "startLink": "https://example.com",
        "startTime": "string",
        "startTimeMillisec": 1,
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
| `session.creatorZuid` | string |  |
| `session.departmentId` | string |  |
| `session.departmentName` | string |  |
| `session.duration` | number |  |
| `session.endTime` | string |  |
| `session.endTimeMillisec` | number |  |
| `session.isDepartmentAdmin` | boolean |  |
| `session.meeting.zsoid` | string |  |
| `session.meetingKey` | string |  |
| `session.offset` | string |  |
| `session.presenter` | number |  |
| `session.presenterEmail` | string |  |
| `session.recurringType` | number |  |
| `session.regEmbedURL` | string |  |
| `session.registrationLink` | string |  |
| `session.sessionType` | string |  |
| `session.startLink` | string |  |
| `session.startTime` | string |  |
| `session.startTimeMillisec` | number |  |
| `session.sys_id` | string |  |
| `session.timezone` | string |  |
| `session.topic` | string |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `POST /api/v2/:organizationId/webinar.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webinar.md) for the provider-specific parameters and requirements.

