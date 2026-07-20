# Hippo Video: Import Video

Imports a video into Hippo Video from a downloadable URL.

```
POST https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/import-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/import-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/import-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Video title |
| `url` | string | yes | Downloadable URL of the video |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "embedUrl": "https://example.com",
      "shareUrl": "https://example.com",
      "status": 1,
      "thumbnailPreview": "string",
      "videoId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `embedUrl` | string |  |
| `shareUrl` | string |  |
| `status` | number |  |
| `thumbnailPreview` | string |  |
| `videoId` | number |  |

## Native endpoint

Through the native Hippo Video API, this operation is `POST /api/v1/me/video/import` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-video.md) for the provider-specific parameters and requirements.

