# Webex: List Meetings

Lists meetings in your Webex account.

```
GET https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-meetings?${params}`, {
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
| `max` | number | no | Maximum number of meetings to return. Example: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenda": "string",
      "allowAnyUserToBeCoHost": true,
      "dialInIpAddress": "string",
      "enabledAutoRecordMeeting": true,
      "enabledJoinBeforeHost": true,
      "end": "2026-05-07T12:00:00.000Z",
      "excludePassword": true,
      "hostDisplayName": "Ava Chen",
      "hostEmail": "ava@example.com",
      "hostUserId": "string",
      "id": "string",
      "joinBeforeHostMinutes": 1,
      "meetingNumber": "string",
      "meetingType": "string",
      "password": "string",
      "phoneAndVideoSystemPassword": "string",
      "publicMeeting": true,
      "recurrence": "string",
      "reminderTime": 1,
      "scheduledType": "string",
      "sessionTypeId": 1,
      "sipAddress": "string",
      "siteUrl": "https://example.com",
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "timezone": "string",
      "title": "string",
      "unlockedMeetingJoinSecurity": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda` | string | Meeting agenda. |
| `allowAnyUserToBeCoHost` | boolean | Whether any user can be co-host. |
| `dialInIpAddress` | string | Dial-in IP address. |
| `enabledAutoRecordMeeting` | boolean | Whether automatic recording is enabled. |
| `enabledJoinBeforeHost` | boolean | Whether participants can join before host. |
| `end` | date | Meeting end time. |
| `excludePassword` | boolean | Whether the password is excluded from invitations. |
| `hostDisplayName` | string | Host display name. |
| `hostEmail` | string | Host email address. |
| `hostUserId` | string | Host user identifier. |
| `id` | string | Meeting identifier. |
| `joinBeforeHostMinutes` | number | Minutes participants can join before host. |
| `meetingNumber` | string | Webex meeting number. |
| `meetingType` | string | Meeting type. |
| `password` | string | Meeting password when returned. |
| `phoneAndVideoSystemPassword` | string | Phone and video system password when returned. |
| `publicMeeting` | boolean | Whether the meeting is public. |
| `recurrence` | string | Recurrence rule for recurring meetings. |
| `reminderTime` | number | Reminder offset in minutes. |
| `scheduledType` | string | Scheduled meeting type. |
| `sessionTypeId` | number | Session type identifier. |
| `sipAddress` | string | SIP address for joining from a video system. |
| `siteUrl` | string | Webex site URL. |
| `start` | date | Meeting start time. |
| `state` | string | Current meeting state. |
| `timezone` | string | Meeting timezone. |
| `title` | string | Meeting title. |
| `unlockedMeetingJoinSecurity` | string | Join security for unlocked meetings. |
| `webLink` | string | Browser link for the meeting. |

## Native endpoint

Through the native Webex API, this operation is `GET /meetings` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

