# Cisco Webex Meetings: Get a Meeting

Retrieves a meeting from Cisco Webex Meetings.

```
GET https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/get-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/get-meeting?connectionId=$CONNECTION_ID&meetingId=25bbf831-5be9-4c25-b4b0-9b592c8a086b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "25bbf831-5be9-4c25-b4b0-9b592c8a086b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/get-meeting?${params}`, {
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
| `meetingId` | string | yes | Unique identifier for the meeting being requested. Example: `25bbf831-5be9-4c25-b4b0-9b592c8a086b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenda": "string",
      "enabledBreakoutSessions": true,
      "end": "string",
      "hostDisplayName": "Ava Chen",
      "hostEmail": "ava@example.com",
      "hostUserId": "string",
      "id": "string",
      "meetingNumber": "string",
      "meetingType": "string",
      "siteUrl": "https://example.com",
      "start": "string",
      "state": "string",
      "telephony": {},
      "timezone": "string",
      "title": "string",
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
| `enabledBreakoutSessions` | boolean | Whether breakout sessions are enabled. |
| `end` | string | Meeting end time in ISO 8601 format. |
| `hostDisplayName` | string | Display name of the meeting host. |
| `hostEmail` | string | Email address of the meeting host. |
| `hostUserId` | string | Unique identifier for the meeting host. |
| `id` | string | Unique identifier for the meeting. |
| `meetingNumber` | string | Meeting number. |
| `meetingType` | string | Meeting type. |
| `siteUrl` | string | Webex site URL for the meeting. |
| `start` | string | Meeting start time in ISO 8601 format. |
| `state` | string | Meeting state. |
| `telephony` | object | Telephony settings for the meeting. |
| `timezone` | string | Meeting timezone. |
| `title` | string | Meeting title. |
| `webLink` | string | Web link for the meeting. |

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `GET /meetings/:meetingId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting.md) for the provider-specific parameters and requirements.

