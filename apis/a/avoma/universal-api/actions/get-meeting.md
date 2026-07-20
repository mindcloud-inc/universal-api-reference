# Avoma: Get Meeting

Retrieves a meeting from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting?${params}`, {
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
| `uuid` | string | yes | Unique ID of the meeting. |
| `includeCrmAssociations` | boolean | no | Whether to include CRM associations in the response. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {
          "email": "ava@example.com",
          "name": "Ava Chen",
          "response_status": "string",
          "uuid": "string"
        }
      ],
      "audio_ready": true,
      "created": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "end_at": "2026-05-07T12:00:00.000Z",
      "is_call": true,
      "is_internal": true,
      "is_private": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "notes_ready": true,
      "organizer_email": "ava@example.com",
      "processing_status": "string",
      "purpose": {
        "label": "string",
        "uuid": "string"
      },
      "recording_state": "string",
      "recording_uuid": "string",
      "start_at": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "subject": "string",
      "transcript_ready": true,
      "transcription_uuid": "string",
      "type": {
        "label": "string",
        "uuid": "string"
      },
      "url": "https://example.com",
      "uuid": "string",
      "video_ready": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees[].email` | string |  |
| `attendees[].name` | string |  |
| `attendees[].response_status` | string |  |
| `attendees[].uuid` | string |  |
| `audio_ready` | boolean |  |
| `created` | date |  |
| `duration` | number |  |
| `end_at` | date |  |
| `is_call` | boolean |  |
| `is_internal` | boolean |  |
| `is_private` | boolean |  |
| `modified` | date |  |
| `notes_ready` | boolean |  |
| `organizer_email` | string |  |
| `processing_status` | string |  |
| `purpose.label` | string |  |
| `purpose.uuid` | string |  |
| `recording_state` | string |  |
| `recording_uuid` | string |  |
| `start_at` | date |  |
| `state` | string |  |
| `subject` | string |  |
| `transcript_ready` | boolean |  |
| `transcription_uuid` | string |  |
| `type.label` | string |  |
| `type.uuid` | string |  |
| `url` | string |  |
| `uuid` | string |  |
| `video_ready` | boolean |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/meetings/:uuid/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting.md) for the provider-specific parameters and requirements.

