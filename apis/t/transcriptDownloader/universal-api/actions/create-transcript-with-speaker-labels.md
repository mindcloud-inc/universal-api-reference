# Transcript Downloader: Create Transcript with Speaker Labels

Creates a transcript with speaker labels in Transcript Downloader.

```
POST https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-transcript-with-speaker-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-transcript-with-speaker-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transcriptWithSpeakerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-transcript-with-speaker-labels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transcriptWithSpeakerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transcriptWithSpeakerId` | string | yes | The transcript_speaker_id returned from an audio download response. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "duration": 1,
        "language": "string",
        "message": "string",
        "transcriptsWithTimeStamps": [
          {
            "duration": 1,
            "speaker": "string",
            "start": 1,
            "text": "string"
          }
        ]
      },
      "mediaId": "string",
      "message": "string",
      "status": "string",
      "transcriptSpeakerCost": "string",
      "transcriptSpeakerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.duration` | number |  |
| `data.language` | string |  |
| `data.message` | string |  |
| `data.transcriptsWithTimeStamps` | array<object> |  |
| `data.transcriptsWithTimeStamps[].duration` | number |  |
| `data.transcriptsWithTimeStamps[].speaker` | string |  |
| `data.transcriptsWithTimeStamps[].start` | number |  |
| `data.transcriptsWithTimeStamps[].text` | string |  |
| `mediaId` | string |  |
| `message` | string |  |
| `status` | string |  |
| `transcriptSpeakerCost` | string |  |
| `transcriptSpeakerId` | string |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `POST /api/transcriptspeakerid` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcript-with-speaker-labels.md) for the provider-specific parameters and requirements.

