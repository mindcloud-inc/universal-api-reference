# YouTube: Set Thumbnail

Sets a custom thumbnail for a YouTube video.

```
PUT https://connect.mindcloud.co/v1/universal/youtube/latest/actions/set-thumbnail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/set-thumbnail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string",
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youtube/latest/actions/set-thumbnail', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string",
    "image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes | ID of the video for which the custom thumbnail is being provided. |
| `image` | file | yes | Binary image file to upload as the custom thumbnail. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onBehalfOfContentOwner` | string | no | Content owner ID when acting on behalf of a CMS user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default": {
        "height": 1,
        "url": "https://example.com",
        "width": 1
      },
      "high": {
        "height": 1,
        "url": "https://example.com",
        "width": 1
      },
      "medium": {
        "height": 1,
        "url": "https://example.com",
        "width": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default.height` | number |  |
| `default.url` | string |  |
| `default.width` | number |  |
| `high.height` | number |  |
| `high.url` | string |  |
| `high.width` | number |  |
| `medium.height` | number |  |
| `medium.url` | string |  |
| `medium.width` | number |  |

## Native endpoint

Through the native YouTube API, this operation is `POST /upload/youtube/v3/thumbnails/set` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-thumbnail.md) for the provider-specific parameters and requirements.

