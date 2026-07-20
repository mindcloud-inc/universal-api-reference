# Speak Ai: Get Media Transcript

Retrieves a media transcript from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-media-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-media-transcript?connectionId=$CONNECTION_ID&mediaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-media-transcript?${params}`, {
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
| `mediaId` | string | yes | Speak Ai media identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aws": {
        "isArchived": true
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": {
        "end": "string",
        "inSecond": 1,
        "start": "string"
      },
      "folderId": "string",
      "insight": {
        "speakers": [
          {
            "duration": 1,
            "id": 1,
            "name": "Ava Chen",
            "totalWords": 1,
            "wpm": 1
          }
        ],
        "transcript": [
          {
            "confidence": 1,
            "id": 1,
            "instances": [
              {
                "end": "string",
                "endInSec": 1,
                "start": "string",
                "startInSec": 1
              }
            ],
            "language": "string",
            "speakerId": "string",
            "text": "string"
          }
        ]
      },
      "mediaId": "string",
      "mediaType": "string",
      "mediaUrl": "https://example.com",
      "name": "Ava Chen",
      "sourceLanguage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aws.isArchived` | boolean |  |
| `createdAt` | date |  |
| `duration.end` | string |  |
| `duration.inSecond` | number |  |
| `duration.start` | string |  |
| `folderId` | string |  |
| `insight.speakers[].duration` | number |  |
| `insight.speakers[].id` | number |  |
| `insight.speakers[].name` | string |  |
| `insight.speakers[].totalWords` | number |  |
| `insight.speakers[].wpm` | number |  |
| `insight.transcript[].confidence` | number |  |
| `insight.transcript[].id` | number |  |
| `insight.transcript[].instances[].end` | string |  |
| `insight.transcript[].instances[].endInSec` | number |  |
| `insight.transcript[].instances[].start` | string |  |
| `insight.transcript[].instances[].startInSec` | number |  |
| `insight.transcript[].language` | string |  |
| `insight.transcript[].speakerId` | string |  |
| `insight.transcript[].text` | string |  |
| `mediaId` | string |  |
| `mediaType` | string |  |
| `mediaUrl` | string |  |
| `name` | string |  |
| `sourceLanguage` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /media/transcript/:mediaId` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-transcript.md) for the provider-specific parameters and requirements.

