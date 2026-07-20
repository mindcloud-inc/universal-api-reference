# Zoho Meeting: Get Meeting Details

Retrieves meeting details from Zoho Meeting.

```
GET https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-meeting-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-meeting-details?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D&meetingKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}",
  "meetingKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/get-meeting-details?${params}`, {
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
| `meetingKey` | string | yes | Meeting key returned by List Meetings or Create Meeting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenda": "string",
      "audioConference": {
        "type": 1
      },
      "departmentId": "string",
      "departmentName": "Ava Chen",
      "duration": "string",
      "durationInHours": "string",
      "encryptPwd": "string",
      "endTime": "string",
      "eTime": "string",
      "eventId": "string",
      "isCreatorUser": true,
      "isDepartmentAdmin": true,
      "isE2E": true,
      "isJoinBeforeHostAllowed": true,
      "isOtherOrg": true,
      "isPastSession": true,
      "isStaticMeeting": true,
      "isVideoMeeting": true,
      "joinLink": "https://example.com",
      "meetingEmbedUrl": "https://example.com",
      "meetingKey": "string",
      "presenter": "string",
      "presenterEmail": "ava@example.com",
      "presenterName": "Ava Chen",
      "pwd": "string",
      "reminderDetails": [
        {
          "reminderDateTime": "string",
          "reminderTime": 1,
          "timeFormat": "string"
        }
      ],
      "sDate": "string",
      "shortenJoinUrl": "https://example.com",
      "startLink": "https://example.com",
      "startTime": "string",
      "startTimeMillisec": 1,
      "status": 1,
      "sTime": "string",
      "timeFormat": "string",
      "timePeriod": "string",
      "timezone": "string",
      "timeZoneOriginal": "string",
      "topic": "string",
      "transcriptionLanguageCode": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda` | string |  |
| `audioConference.type` | number |  |
| `departmentId` | string |  |
| `departmentName` | string |  |
| `duration` | string |  |
| `durationInHours` | string |  |
| `encryptPwd` | string |  |
| `endTime` | string |  |
| `eTime` | string |  |
| `eventId` | string |  |
| `isCreatorUser` | boolean |  |
| `isDepartmentAdmin` | boolean |  |
| `isE2E` | boolean |  |
| `isJoinBeforeHostAllowed` | boolean |  |
| `isOtherOrg` | boolean |  |
| `isPastSession` | boolean |  |
| `isStaticMeeting` | boolean |  |
| `isVideoMeeting` | boolean |  |
| `joinLink` | string |  |
| `meetingEmbedUrl` | string |  |
| `meetingKey` | string |  |
| `presenter` | string |  |
| `presenterEmail` | string |  |
| `presenterName` | string |  |
| `pwd` | string |  |
| `reminderDetails[].reminderDateTime` | string |  |
| `reminderDetails[].reminderTime` | number |  |
| `reminderDetails[].timeFormat` | string |  |
| `sDate` | string |  |
| `shortenJoinUrl` | string |  |
| `startLink` | string |  |
| `startTime` | string |  |
| `startTimeMillisec` | number |  |
| `status` | number |  |
| `sTime` | string |  |
| `timeFormat` | string |  |
| `timePeriod` | string |  |
| `timezone` | string |  |
| `timeZoneOriginal` | string |  |
| `topic` | string |  |
| `transcriptionLanguageCode` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `GET /api/v2/:organizationId/sessions/:meetingKey.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-details.md) for the provider-specific parameters and requirements.

