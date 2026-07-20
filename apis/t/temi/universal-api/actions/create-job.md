# Temi: Create Job

Creates a transcription job in Temi.

```
POST https://connect.mindcloud.co/v1/universal/temi/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/temi/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaUrl": "https://example.com/audio.wav"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/temi/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaUrl": "https://example.com/audio.wav"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaUrl` | string | yes | Public URL of the audio or video file to transcribe. Example: `https://example.com/audio.wav`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional URL Temi should call when the job completes or fails. Example: `https://example.com/temi-callback`. |
| `metadata` | string | no | Optional metadata to associate with the submitted job. Example: `Customer case 123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_on": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "metadata": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_on` | date | Job creation timestamp. |
| `id` | string | Temi job ID. |
| `metadata` | string | Metadata associated with the job. |
| `status` | string | Initial job status. |

## Native endpoint

Through the native Temi API, this operation is `POST /jobs` (base URL `https://api.temi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

