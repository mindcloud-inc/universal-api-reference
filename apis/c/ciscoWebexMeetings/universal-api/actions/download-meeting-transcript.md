# Cisco Webex Meetings: Download a Meeting Transcript

Retrieves a downloadable meeting transcript from Cisco Webex Meetings.

```
GET https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/download-meeting-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cisco Webex Meetings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/download-meeting-transcript?connectionId=$CONNECTION_ID&transcriptId=d93cf026-739d-4c27-bc80-d2c4795560eb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "d93cf026-739d-4c27-bc80-d2c4795560eb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/download-meeting-transcript?${params}`, {
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
| `transcriptId` | string | yes | Unique identifier for the meeting transcript to download. Example: `d93cf026-739d-4c27-bc80-d2c4795560eb`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cisco Webex Meetings API returns.

## Native endpoint

Through the native Cisco Webex Meetings API, this operation is `GET /meetingTranscripts/:transcriptId/download` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-meeting-transcript.md) for the provider-specific parameters and requirements.

