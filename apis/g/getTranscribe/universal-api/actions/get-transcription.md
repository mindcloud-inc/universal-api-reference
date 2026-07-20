# GetTranscribe: Get Transcription

Retrieves a transcription from GetTranscribe by ID.

```
GET https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/get-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetTranscribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/get-transcription?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/get-transcription?${params}`, {
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
| `id` | number | yes | The ID of the transcription to retrieve. |

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
      "userCity": "string",
      "userCountry": "string",
      "userCountryCode": "string",
      "userId": 1,
      "userIp": "string",
      "userLatitude": 1,
      "userLongitude": 1,
      "userOrg": "string",
      "userRegion": "string",
      "userTimezone": "string",
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
| `userCity` | string |  |
| `userCountry` | string |  |
| `userCountryCode` | string |  |
| `userId` | number |  |
| `userIp` | string |  |
| `userLatitude` | number |  |
| `userLongitude` | number |  |
| `userOrg` | string |  |
| `userRegion` | string |  |
| `userTimezone` | string |  |
| `videoDescription` | string |  |
| `videoHeight` | number |  |
| `videoTitle` | string |  |
| `videoWidth` | number |  |
| `viewCount` | number |  |
| `wordCount` | number |  |

## Native endpoint

Through the native GetTranscribe API, this operation is `GET /transcriptions/:id` (base URL `https://api.gettranscribe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription.md) for the provider-specific parameters and requirements.

