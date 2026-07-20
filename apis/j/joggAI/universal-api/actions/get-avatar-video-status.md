# JoggAI: Get Avatar Video Status



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-avatar-video-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-avatar-video-status?connectionId=$CONNECTION_ID&videoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-avatar-video-status?${params}`, {
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
| `videoId` | string | yes | The avatar video ID returned when a video is created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coverUrl": "https://example.com",
      "createdAt": 1,
      "status": "string",
      "videoId": "string",
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverUrl` | string |  |
| `createdAt` | number |  |
| `status` | string |  |
| `videoId` | string |  |
| `videoUrl` | string |  |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/avatar_video/{videoId}` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-video-status.md) for the provider-specific parameters and requirements.

