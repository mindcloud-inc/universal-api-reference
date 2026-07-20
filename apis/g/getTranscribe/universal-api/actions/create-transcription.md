# GetTranscribe: Create Transcription

Creates a transcription in GetTranscribe from a video URL.

```
POST https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/create-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetTranscribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/create-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/create-transcription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The video URL to transcribe. |
| `folderId` | number | no | Optional folder ID for organization. |
| `language` | string | no | Optional ISO-639-1 language code. |
| `model` | string | no | Optional transcription profile. One of: `0`, `1`, `2`, `3`. |
| `prompt` | string | no | Optional context text to guide transcription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisLanguage": "string",
      "author": "string",
      "authorId": "string",
      "channel": "string",
      "charCount": 1,
      "commentCount": 1,
      "consumptionType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "downloadAudioUrl": "https://example.com",
      "downloadMethod": "string",
      "downloadVideoUrl": "https://example.com",
      "duration": 1,
      "durationSeconds": 1,
      "folderId": 1,
      "generatedTitle": "string",
      "id": 1,
      "language": "string",
      "likeCount": 1,
      "openaiTranscriptionAnalysisCost": "string",
      "openaiTranscriptionAnalysisModel": "string",
      "originalTranscription": "string",
      "platform": "string",
      "prompt": "string",
      "proxyProvider": "string",
      "proxyUsed": true,
      "rawMetadata": "string",
      "relationFolder": {},
      "s3AudioPath": "string",
      "s3ThumbnailPath": "string",
      "s3VideoPath": "string",
      "source": "string",
      "thumbnailUrl": "https://example.com",
      "transcription": "string",
      "transcriptionAnalysis": {},
      "transcriptionSegments": [
        {}
      ],
      "transcriptionWords": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadDate": "string",
      "uploadTimestamp": "string",
      "url": "https://example.com",
      "userId": 1,
      "videoDescription": "string",
      "videoHeight": 1,
      "videoTitle": "string",
      "videoWidth": 1,
      "viewCount": 1,
      "wordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisLanguage` | string |  |
| `author` | string |  |
| `authorId` | string |  |
| `channel` | string |  |
| `charCount` | number |  |
| `commentCount` | number |  |
| `consumptionType` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `downloadAudioUrl` | string |  |
| `downloadMethod` | string |  |
| `downloadVideoUrl` | string |  |
| `duration` | number |  |
| `durationSeconds` | number |  |
| `folderId` | number |  |
| `generatedTitle` | string |  |
| `id` | number |  |
| `language` | string |  |
| `likeCount` | number |  |
| `openaiTranscriptionAnalysisCost` | string |  |
| `openaiTranscriptionAnalysisModel` | string |  |
| `originalTranscription` | string |  |
| `platform` | string |  |
| `prompt` | string |  |
| `proxyProvider` | string |  |
| `proxyUsed` | boolean |  |
| `rawMetadata` | string |  |
| `relationFolder` | object |  |
| `s3AudioPath` | string |  |
| `s3ThumbnailPath` | string |  |
| `s3VideoPath` | string |  |
| `source` | string |  |
| `thumbnailUrl` | string |  |
| `transcription` | string |  |
| `transcriptionAnalysis` | object |  |
| `transcriptionSegments` | array<object> |  |
| `transcriptionWords` | array<object> |  |
| `updatedAt` | date |  |
| `uploadDate` | string |  |
| `uploadTimestamp` | string |  |
| `url` | string |  |
| `userId` | number |  |
| `videoDescription` | string |  |
| `videoHeight` | number |  |
| `videoTitle` | string |  |
| `videoWidth` | number |  |
| `viewCount` | number |  |
| `wordCount` | number |  |

## Native endpoint

Through the native GetTranscribe API, this operation is `POST /transcriptions` (base URL `https://api.gettranscribe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription.md) for the provider-specific parameters and requirements.

