# Vimeo: List Showcase Videos

Retrieves videos in a Vimeo showcase.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-showcase-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-showcase-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=152184&albumId=40988" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "152184",
  "albumId": "40988"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-showcase-videos?${params}`, {
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
| `userId` | number | yes | The ID of the user. Example: `152184`. |
| `albumId` | number | yes | The ID of the showcase. Example: `40988`. |
| `query` | string | no | The search query to use to filter the results. Example: `Stop motion`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | list<string> | no | The way to sort the results. One of: `alphabetical`, `comments`, `date`, `default`, `duration`, `likes`, `manual`, `modified_time`, `plays`. Example: `date`. |
| `direction` | list<string> | no | The sort direction of the results. One of: `asc`, `desc`. Example: `asc`. |
| `filter` | list<string> | no | The attribute by which to filter the results. One of: `embeddable`, `playable`. Example: `embeddable`. |
| `filterEmbeddable` | boolean | no | Whether to filter by embeddable videos when filter is embeddable. Example: `true`. |
| `containingUri` | string | no | The page containing the video URI. Example: `/videos/258684937`. |
| `password` | string | no | The password of the showcase. Example: `hunter1`. |
| `weakSearch` | boolean | no | Whether to include private videos in the search. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentRatingClass": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "hasAudio": true,
      "height": 1,
      "isPlayable": true,
      "link": "https://example.com",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "playerEmbedUrl": "https://example.com",
      "releaseTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string",
      "uri": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentRatingClass` | string | The content rating class. |
| `createdTime` | date | When the video was created. |
| `description` | string | The video description. |
| `duration` | number | Video duration in seconds. |
| `hasAudio` | boolean | Whether the video has audio. |
| `height` | number | Video height in pixels. |
| `isPlayable` | boolean | Whether the video is playable. |
| `link` | string | The public Vimeo video URL. |
| `modifiedTime` | date | When the video was last modified. |
| `name` | string | The video name. |
| `playerEmbedUrl` | string | The embeddable player URL. |
| `releaseTime` | date | When the video was released. |
| `status` | string | The current video availability status. |
| `type` | string | The resource type. |
| `uri` | string | The video API URI. |
| `width` | number | Video width in pixels. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /users/:user_id/albums/:album_id/videos` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-showcase-videos.md) for the provider-specific parameters and requirements.

