# Zoho Meeting: Get Webinar Details

Retrieves webinar details from Zoho Meeting.

```
GET https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-webinar-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-webinar-details?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D&webinarKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-webinar-details?${params}`, {
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
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |
| `webinarKey` | string | yes | Webinar key returned by List Webinars or Create Webinar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "session": {
        "agenda": "string",
        "attendeesCount": 1,
        "contactEmail": "ava@example.com",
        "creatorZuid": "string",
        "departmentId": "string",
        "departmentName": "Ava Chen",
        "digest": "string",
        "displayName": "Ava Chen",
        "duration": 1,
        "endTime": "string",
        "endtimeFormat": "string",
        "endTimeMillisec": 1,
        "instanceId": "string",
        "isDepartmentAdmin": true,
        "isPastSession": true,
        "isSessionStarted": true,
        "meetingKey": "string",
        "offset": "string",
        "presenter": "string",
        "presenterEmail": "ava@example.com",
        "regEmbedURL": "https://example.com",
        "registrationCount": 1,
        "registrationLink": "https://example.com",
        "registrationRequired": true,
        "service": 1,
        "startLink": "https://example.com",
        "startTime": "string",
        "startTimeMillisec": 1,
        "timeFormat": "string",
        "timezone": "string",
        "topic": "string",
        "webinarType": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `session.agenda` | string |  |
| `session.attendeesCount` | number |  |
| `session.contactEmail` | string |  |
| `session.creatorZuid` | string |  |
| `session.departmentId` | string |  |
| `session.departmentName` | string |  |
| `session.digest` | string |  |
| `session.displayName` | string |  |
| `session.duration` | number |  |
| `session.endTime` | string |  |
| `session.endtimeFormat` | string |  |
| `session.endTimeMillisec` | number |  |
| `session.instanceId` | string |  |
| `session.isDepartmentAdmin` | boolean |  |
| `session.isPastSession` | boolean |  |
| `session.isSessionStarted` | boolean |  |
| `session.meetingKey` | string |  |
| `session.offset` | string |  |
| `session.presenter` | string |  |
| `session.presenterEmail` | string |  |
| `session.regEmbedURL` | string |  |
| `session.registrationCount` | number |  |
| `session.registrationLink` | string |  |
| `session.registrationRequired` | boolean |  |
| `session.service` | number |  |
| `session.startLink` | string |  |
| `session.startTime` | string |  |
| `session.startTimeMillisec` | number |  |
| `session.timeFormat` | string |  |
| `session.timezone` | string |  |
| `session.topic` | string |  |
| `session.webinarType` | number |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `GET /api/v2/:organizationId/webinar/:webinarKey.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webinar-details.md) for the provider-specific parameters and requirements.

