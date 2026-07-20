# Twitch: List Videos

Retrieves video records and metadata from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-videos?${params}`, {
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
| `id` | string | no | An ID that identifies the video to get. Specify this parameter up to 100 times. Accepts multiple values as an array. |
| `userId` | string | no | The ID of the user who owns the video. |
| `gameId` | string | no | The ID of the game whose videos you want to get. |
| `language` | string | no | A filter to limit the response to videos in the specified language. |
| `period` | string | no | A filter that determines the period during which the video was created. |
| `sort` | string | no | Sort order for the results. Valid values are time, trending, and views. |
| `type` | string | no | Filter videos by type. Valid values are all, upload, archive, and highlight. |
| `first` | number | no | Maximum number of videos to return. Minimum 1, maximum 100. |
| `after` | string | no | Cursor for forward pagination. |
| `before` | string | no | Cursor for backward pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "duration": "string",
      "id": "string",
      "language": "string",
      "mutedSegments": {},
      "publishedAt": "string",
      "streamId": "string",
      "thumbnailUrl": "https://example.com",
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "userId": "string",
      "userLogin": "string",
      "userName": "Ava Chen",
      "viewable": "string",
      "viewCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `duration` | string |  |
| `id` | string |  |
| `language` | string |  |
| `mutedSegments` | object |  |
| `publishedAt` | string |  |
| `streamId` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `userId` | string |  |
| `userLogin` | string |  |
| `userName` | string |  |
| `viewable` | string |  |
| `viewCount` | number |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /videos` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.

