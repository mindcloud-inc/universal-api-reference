# YouTube: List Captions

Retrieves caption tracks for a YouTube video.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-captions?connectionId=$CONNECTION_ID&part=snippet&videoId=dQw4w9WgXcQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "part": "snippet",
  "videoId": "dQw4w9WgXcQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-captions?${params}`, {
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
| `part` | string | yes | Accepts multiple values in one string, delimited by `,`. Example: `snippet`. |
| `videoId` | string | yes | Example: `dQw4w9WgXcQ`. |
| `id` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `AbCdEf1234567890,ZXCVBN0987654321`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onBehalfOf` | string | no |  |
| `onBehalfOfContentOwner` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {
        "isCC": true,
        "language": "string",
        "lastUpdated": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "status": "string",
        "trackKind": "string",
        "videoId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet.isCC` | boolean |  |
| `snippet.language` | string |  |
| `snippet.lastUpdated` | date |  |
| `snippet.name` | string |  |
| `snippet.status` | string |  |
| `snippet.trackKind` | string |  |
| `snippet.videoId` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/captions` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-captions.md) for the provider-specific parameters and requirements.

