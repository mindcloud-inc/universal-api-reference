# Orshot: Upload Brand Video



```
POST https://connect.mindcloud.co/v1/universal/orshot/latest/actions/upload-brand-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/upload-brand-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/upload-brand-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | The video file content or source. |
| `fileName` | string | no | The uploaded video filename. |
| `tags[]` | array<string> | no | Tags to associate with the video. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "url": "https://example.com",
        "video": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "directUrl": "https://example.com",
          "duration": 1,
          "fileSize": 1,
          "format": "string",
          "height": 1,
          "id": 1,
          "metadata": {},
          "mimeType": "string",
          "name": "Ava Chen",
          "originalFilename": "Ava Chen",
          "tags": [
            "string"
          ],
          "thumbnailUrl": "https://example.com",
          "userId": "string",
          "width": 1,
          "workspaceId": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.url` | string | Convenience direct URL for the uploaded video asset. |
| `data.video.createdAt` | date | Timestamp when the video asset was created. |
| `data.video.directUrl` | string | Direct URL for the stored video asset. |
| `data.video.duration` | number | Video duration when available. |
| `data.video.fileSize` | number | Video asset file size in bytes. |
| `data.video.format` | string | Video file format. |
| `data.video.height` | number | Video height when available. |
| `data.video.id` | number | Uploaded video asset identifier. |
| `data.video.metadata` | object | Provider metadata returned for the video asset. |
| `data.video.mimeType` | string | Video MIME type. |
| `data.video.name` | string | Stored asset name. |
| `data.video.originalFilename` | string | Original uploaded filename. |
| `data.video.tags` | array<string> | Tags assigned to the video asset. |
| `data.video.thumbnailUrl` | string | Thumbnail URL when available. |
| `data.video.userId` | string | User that created the video asset. |
| `data.video.width` | number | Video width when available. |
| `data.video.workspaceId` | number | Workspace that owns the video asset. |

## Native endpoint

Through the native Orshot API, this operation is `POST /brand-assets/videos/add` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-brand-video.md) for the provider-specific parameters and requirements.

