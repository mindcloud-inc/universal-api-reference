# Speech is Cheap: Create Transcription Job

Creates a new transcription job in Speech is Cheap.

```
POST https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/create-transcription-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speech is Cheap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/create-transcription-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputUrl": "https://example.com/audio-file.mp3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/create-transcription-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputUrl": "https://example.com/audio-file.mp3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputUrl` | string | yes | Publicly accessible audio or video file URL to transcribe. Example: `https://example.com/audio-file.mp3`. |
| `webhookUrl` | string | no | Optional URL where Speech is Cheap may POST transcription results. Example: `https://your-domain.com/webhook`. |
| `language` | string | no | Optional two-letter ISO 639-1 language code, such as en or es. Omit for auto-detection. Example: `en`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `canLabelAudio` | boolean | no | When enabled, includes audio classification labels in transcription output. |
| `canParseSpeakers` | boolean | no | When enabled, includes speaker_id on each segment. |
| `canParseWords` | boolean | no | When enabled, includes timestamps for each word. |
| `isPrivate` | boolean | no | When enabled, redacts the original input_url and deletes segments after 12 hours. |
| `minimumConfidence` | number | no | Filters out segments below this confidence threshold. Defaults to 0.5. Example: `0.5`. |
| `segmentDuration` | number | no | Transcription segment duration in seconds. Must be between 6 and 30. Example: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "output": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Speech is Cheap transcription job identifier. |
| `output` | object | Job output object. It is empty when an asynchronous job is first accepted. |
| `status` | string | Job status returned after creation, such as PENDING. |

## Native endpoint

Through the native Speech is Cheap API, this operation is `POST /jobs/` (base URL `https://api.speechischeap.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription-job.md) for the provider-specific parameters and requirements.

