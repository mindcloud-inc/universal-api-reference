# VideoDB: Get Video Transcription

Retrieves a video transcription from VideoDB.

```
GET https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/get-video-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VideoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/get-video-transcription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/get-video-transcription?${params}`, {
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
| `videoId` | string | no | Video ID whose transcription should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string",
      "word_timestamps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string | Transcript text. |
| `word_timestamps` | array<object> | Word timestamp segments. |

## Native endpoint

Through the native VideoDB API, this operation is `GET /video/:video_id/transcription/` (base URL `https://api.videodb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-transcription.md) for the provider-specific parameters and requirements.

