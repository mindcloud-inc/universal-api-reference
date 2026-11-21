# Facebook: Create Page Video



```
POST https://connect.mindcloud.co/v1/universal/facebook/latest/actions/create-page-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Facebook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/create-page-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "fileUrl": "https://example.com/video.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/facebook/latest/actions/create-page-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "fileUrl": "https://example.com/video.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | list<string> | yes |  |
| `fileUrl` | string | yes | Publicly accessible URL of the video file. Example: `https://example.com/video.mp4`. |
| `title` | string | no |  |
| `description` | string | no | Text for the post about the video. |
| `published` | boolean | no | Set to false to create an unpublished video post. Default: `true`. |
| `scheduledPublishTime` | date | no | 10 minutes to 6 months from now. Set Published to false when scheduling. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Facebook API returns.

## Native endpoint

Through the native Facebook API, this operation is `POST /:pageId/videos` (base URL `https://graph.facebook.com/v25.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page-video.md) for the provider-specific parameters and requirements.

