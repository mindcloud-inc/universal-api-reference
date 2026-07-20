# YouTube: Update Video

Updates an existing video in YouTube.

```
PUT https://connect.mindcloud.co/v1/universal/youtube/latest/actions/update-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/update-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "part": "snippet,status",
  "id": "dQw4w9WgXcQ"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youtube/latest/actions/update-video', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "part": "snippet,status",
    "id": "dQw4w9WgXcQ"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `part` | string | yes | Accepts multiple values in one string, delimited by `,`. Example: `snippet,status`. |
| `id` | string | yes | Example: `dQw4w9WgXcQ`. |
| `snippet.title` | string | no |  |
| `snippet.description` | string | no |  |
| `status.privacyStatus` | string | no | Example: `unlisted`. |
| `snippet.tags[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `localizations` | object | no |  |
| `onBehalfOfContentOwner` | string | no |  |

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

Through the native YouTube API, this operation is `PUT /youtube/v3/videos` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video.md) for the provider-specific parameters and requirements.

