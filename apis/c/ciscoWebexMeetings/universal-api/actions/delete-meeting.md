# Cisco Webex Meetings: Delete a Meeting

Deletes an existing meeting from Cisco Webex Meetings.

```
DELETE https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-meeting?connectionId=$CONNECTION_ID&meetingId=25bbf831-5be9-4c25-b4b0-9b592c8a086b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "25bbf831-5be9-4c25-b4b0-9b592c8a086b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-meeting?${params}`, {
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
| `meetingId` | string | yes | Unique identifier for the meeting to delete. Example: `25bbf831-5be9-4c25-b4b0-9b592c8a086b`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cisco Webex Meetings API returns.

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `DELETE /meetings/:meetingId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-meeting.md) for the provider-specific parameters and requirements.

