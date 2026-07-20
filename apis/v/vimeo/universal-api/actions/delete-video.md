# Vimeo: Delete Video

Deletes an existing video from Vimeo.

```
DELETE https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/delete-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/delete-video?connectionId=$CONNECTION_ID&videoId=1146062919" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "1146062919"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/delete-video?${params}`, {
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
| `videoId` | number | yes | The ID of the video. Example: `1146062919`. |

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

Through the native Vimeo API, this operation is `DELETE /videos/:video_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video.md) for the provider-specific parameters and requirements.

