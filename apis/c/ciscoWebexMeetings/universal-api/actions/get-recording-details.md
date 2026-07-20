# Cisco Webex Meetings: Get Recording Details

Retrieves recording details from Cisco Webex Meetings.

```
GET https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/get-recording-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/get-recording-details?connectionId=$CONNECTION_ID&recordingId=b9b32f86-e0d2-451e-9ef6-3f91a8ca9c60" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordingId": "b9b32f86-e0d2-451e-9ef6-3f91a8ca9c60"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/get-recording-details?${params}`, {
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
| `recordingId` | string | yes | Unique identifier for the recording. Example: `b9b32f86-e0d2-451e-9ef6-3f91a8ca9c60`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "string",
      "downloadUrl": "https://example.com",
      "durationSeconds": 1,
      "format": "string",
      "id": "string",
      "meetingId": "string",
      "password": "string",
      "playbackUrl": "https://example.com",
      "serviceType": "string",
      "shareToMe": true,
      "siteUrl": "https://example.com",
      "sizeBytes": 1,
      "status": "string",
      "timeRecorded": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | string | Recording creation time in ISO 8601 format. |
| `downloadUrl` | string | Download link for the recording when available. |
| `durationSeconds` | number | Recording duration in seconds. |
| `format` | string | Recording format. |
| `id` | string | Unique identifier for the recording. |
| `meetingId` | string | Unique identifier for the recording's ended meeting instance. |
| `password` | string | Recording playback password. |
| `playbackUrl` | string | Playback link for the recording. |
| `serviceType` | string | Recording service type. |
| `shareToMe` | boolean | Whether the recording is shared with the current user. |
| `siteUrl` | string | Site URL for the recording. |
| `sizeBytes` | number | Recording size in bytes. |
| `status` | string | Recording status. |
| `timeRecorded` | string | Recording start time in ISO 8601 format. |
| `topic` | string | Recording topic. |

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `GET /recordings/:recordingId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recording-details.md) for the provider-specific parameters and requirements.

