# Cisco Webex Meetings: Update a Meeting

Updates an existing meeting in Cisco Webex Meetings.

```
PUT https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/update-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/update-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingId": "25bbf831-5be9-4c25-b4b0-9b592c8a086b"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/update-meeting', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingId": "25bbf831-5be9-4c25-b4b0-9b592c8a086b"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `meetingId` | string | yes | Unique identifier for the meeting to update. Example: `25bbf831-5be9-4c25-b4b0-9b592c8a086b`. |

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
      "meetingSeriesId": "string",
      "meetingType": "string",
      "scheduledMeetingId": "string",
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
| `meetingSeriesId` | string | Unique identifier for the parent meeting series. |
| `meetingType` | string | Meeting type. |
| `scheduledMeetingId` | string | Unique identifier for the scheduled meeting associated with the instance. |
| `siteUrl` | string | Webex site URL for the meeting. |
| `start` | string | Meeting start time in ISO 8601 format. |
| `state` | string | Meeting state. |
| `telephony` | object | Telephony settings for the meeting. |
| `timezone` | string | Meeting timezone. |
| `title` | string | Meeting title. |
| `webLink` | string | Web link for the meeting. |

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `PUT /meetings/:meetingId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-meeting.md) for the provider-specific parameters and requirements.

