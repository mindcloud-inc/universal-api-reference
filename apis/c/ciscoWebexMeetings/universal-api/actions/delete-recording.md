# Cisco Webex Meetings: Delete a Recording

Deletes an existing recording from Cisco Webex Meetings.

```
DELETE https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-recording?connectionId=$CONNECTION_ID&recordingId=b9b32f86-e0d2-451e-9ef6-3f91a8ca9c60" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordingId": "b9b32f86-e0d2-451e-9ef6-3f91a8ca9c60"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/delete-recording?${params}`, {
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
| `recordingId` | string | yes | Unique identifier for the recording to delete. Example: `b9b32f86-e0d2-451e-9ef6-3f91a8ca9c60`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cisco Webex Meetings API returns.

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `DELETE /recordings/:recordingId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-recording.md) for the provider-specific parameters and requirements.

