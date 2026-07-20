# Vimeo: Remove Video from Showcase

Deletes a video from a showcase in Vimeo.

```
DELETE https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/remove-video-from-showcase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/remove-video-from-showcase?connectionId=$CONNECTION_ID&userId=1&albumId=1&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1",
  "albumId": "1",
  "videoId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/remove-video-from-showcase?${params}`, {
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
| `userId` | number | yes | The ID of the user who owns the showcase. |
| `albumId` | number | yes | The ID of the showcase. |
| `videoId` | number | yes | The ID of the video to remove from the showcase. |

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

Through the native Vimeo API, this operation is `DELETE /users/:user_id/albums/:album_id/videos/:video_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-video-from-showcase.md) for the provider-specific parameters and requirements.

