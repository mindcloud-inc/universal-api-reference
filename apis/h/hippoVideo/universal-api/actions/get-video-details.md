# Hippo Video: Get Video Details

Retrieves details for a Hippo Video video.

```
GET https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-video-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-video-details?connectionId=$CONNECTION_ID&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-video-details?${params}`, {
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
| `videoId` | number | yes | ID of the video |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        [
          {}
        ]
      ],
      "code": 1,
      "createdAt": "string",
      "description": "string",
      "displayDate": "string",
      "emailEmbed": "ava@example.com",
      "embedUrl": "https://example.com",
      "id": 1,
      "shareThumbnail": "string",
      "shareUrl": "https://example.com",
      "tags": [
        [
          "string"
        ]
      ],
      "thumbnail": "string",
      "title": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[]` | array<object> |  |
| `categories[].id` | number |  |
| `categories[].name` | string |  |
| `code` | number |  |
| `createdAt` | string |  |
| `description` | string |  |
| `displayDate` | string |  |
| `emailEmbed` | string |  |
| `embedUrl` | string |  |
| `id` | number |  |
| `shareThumbnail` | string |  |
| `shareUrl` | string |  |
| `tags[]` | array<string> |  |
| `thumbnail` | string |  |
| `title` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Hippo Video API, this operation is `GET /api/v1/me/video/:video_id` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-details.md) for the provider-specific parameters and requirements.

