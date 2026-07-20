# Vadootv: Get video URL

Retrieves a generated video URL from Vadootv.

```
GET https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-video-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-video-url?connectionId=$CONNECTION_ID&id=vid%20or%20request_id%20from%20a%20generation%20response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "vid or request_id from a generation response"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-video-url?${params}`, {
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
| `id` | string | yes | The video ID returned by a generation endpoint. Example: `vid or request_id from a generation response`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "progress": 1,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message when generation fails. |
| `progress` | number | Progress percent when the video is still processing. |
| `status` | string | Video generation status. |
| `url` | string | Rendered video URL when complete. |

## Native endpoint

Through the native Vadootv API, this operation is `GET /api/get_video_url` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-url.md) for the provider-specific parameters and requirements.

