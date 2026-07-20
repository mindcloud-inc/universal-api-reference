# Vimeo: Add Video to Showcase

Adds a video to a showcase in Vimeo.

```
POST https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-showcase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-showcase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "albumId": 1,
  "videoId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-showcase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "albumId": 1,
    "videoId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | The ID of the user who owns the showcase. |
| `albumId` | number | yes | The ID of the showcase. |
| `videoId` | number | yes | The ID of the video to add to the showcase. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. Vimeo returns an empty string on successful 204 No Content mutations. |

## Native endpoint

Through the native Vimeo API, this operation is `PUT /users/:user_id/albums/:album_id/videos/:video_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-video-to-showcase.md) for the provider-specific parameters and requirements.

