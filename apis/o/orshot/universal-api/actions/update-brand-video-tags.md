# Orshot: Update Brand Video Tags



```
PUT https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-video-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-video-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-video-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The brand video ID. |
| `tags[]` | array<string> | yes | The tags to set on the video, replacing existing tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the video asset was created. |
| `directUrl` | string | Direct URL for the stored video asset. |
| `duration` | number | Video duration when available. |
| `fileSize` | number | Video asset file size in bytes. |
| `format` | string | Video file format. |
| `height` | number | Video height when available. |
| `id` | number | Brand video asset identifier. |
| `metadata` | object | Provider metadata returned for the video asset. |
| `mimeType` | string | Video MIME type. |
| `name` | string | Stored asset name. |
| `originalFilename` | string | Original uploaded filename. |
| `tags` | array<string> | Tags assigned to the video asset. |
| `thumbnailUrl` | string | Thumbnail URL when available. |
| `userId` | string | User that created the video asset. |
| `width` | number | Video width when available. |
| `workspaceId` | number | Workspace that owns the video asset. |

## Native endpoint

Through the native Orshot API, this operation is `PATCH /brand-assets/videos/update/:id` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-brand-video-tags.md) for the provider-specific parameters and requirements.

