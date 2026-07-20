# YouTube: Upload Video

Uploads a new video to YouTube.

```
POST https://connect.mindcloud.co/v1/universal/youtube/latest/actions/upload-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/upload-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "part": "snippet,status",
  "snippet.title": "My New Video",
  "snippet.categoryId": "22",
  "mediaFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youtube/latest/actions/upload-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "part": "snippet,status",
    "snippet.title": "My New Video",
    "snippet.categoryId": "22",
    "mediaFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `part` | string | yes | Accepts multiple values in one string, delimited by `,`. Default: `snippet,status`. Example: `snippet,status`. |
| `snippet.title` | string | yes | Example: `My New Video`. |
| `snippet.description` | string | no | Example: `Video description`. |
| `snippet.categoryId` | string | yes | YouTube video category ID. Required when the upload includes the snippet part. Default: `22`. |
| `status.privacyStatus` | string | no | Default: `private`. Example: `private`. |
| `snippet.tags[]` | array<string> | no |  |
| `mediaFile` | file | yes | Binary video media file to upload. |
| `notifySubscribers` | boolean | no | Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoLevels` | boolean | no |  |
| `stabilize` | boolean | no |  |
| `onBehalfOfContentOwner` | string | no |  |
| `onBehalfOfContentOwnerChannel` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentDetails": {
        "duration": "string"
      },
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {
        "channelId": "string",
        "description": "string",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "title": "string"
      },
      "statistics": {
        "viewCount": "string"
      },
      "status": {
        "privacyStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentDetails.duration` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet.channelId` | string |  |
| `snippet.description` | string |  |
| `snippet.publishedAt` | date |  |
| `snippet.title` | string |  |
| `statistics.viewCount` | string |  |
| `status.privacyStatus` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `POST /upload/youtube/v3/videos` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video.md) for the provider-specific parameters and requirements.

