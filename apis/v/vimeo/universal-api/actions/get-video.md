# Vimeo: Get Video

Retrieves a video record from Vimeo.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-video?connectionId=$CONNECTION_ID&videoId=1146062919" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "1146062919"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-video?${params}`, {
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
| `timeLinks` | boolean | no | Whether to return timestamps in the description as links. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "pictures": {},
      "privacy": {},
      "status": "string",
      "tags": [
        {}
      ],
      "uri": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | Video creation time. |
| `description` | string | Video description. |
| `duration` | number | Video duration in seconds. |
| `link` | string | Video link. |
| `name` | string | Video title. |
| `pictures` | object | Video pictures. |
| `privacy` | object | Video privacy settings. |
| `status` | string | Video status. |
| `tags` | array<object> | Video tags. |
| `uri` | string | Video URI. |
| `user` | object | Video owner. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /videos/:video_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

