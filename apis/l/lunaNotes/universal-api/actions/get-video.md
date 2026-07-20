# LunaNotes: Get Video

Retrieves a video from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-video?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-video?${params}`, {
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
| `id` | string | yes | The LunaNotes video ID. |
| `include` | string | no | Include related folder, transcripts, summaries, or notes in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "channelTitle": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "folderId": "string",
      "id": "string",
      "metadata": {},
      "thumbnailUrl": "https://example.com",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "v": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string | YouTube channel ID. |
| `channelTitle` | string | YouTube channel title. |
| `createdAt` | date | Timestamp when the video record was created. |
| `duration` | number | Video duration in seconds. |
| `folderId` | string | Folder ID when the video is organized in a folder. |
| `id` | string | Unique identifier for the video. |
| `metadata` | object | Provider metadata for the video. |
| `thumbnailUrl` | string | Thumbnail URL when available. |
| `title` | string | Video title. |
| `updatedAt` | date | Timestamp when the video record was last updated. |
| `userId` | string | Owner user ID. |
| `v` | string | Associated YouTube video ID. |

## Native endpoint

Through the native LunaNotes API, this operation is `GET /v1/videos/:id` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

