# Vimeo: List Channel Videos

Retrieves videos in a Vimeo channel.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-channel-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-channel-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-channel-videos?${params}`, {
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
| `channelId` | number | yes | The ID of the channel. |
| `query` | string | no | The search query to use to filter the results. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `containingUri` | string | no | The page that contains the video URI. |
| `filter` | list | no | The attribute by which to filter the results. One of: `embeddable`. |
| `filterEmbeddable` | boolean | no | Whether to filter the results by embeddable or non-embeddable videos. |
| `sizes` | string | no | The pixel dimensions of the image in {width}x{height} format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {},
      "categories": [
        {}
      ],
      "contentRating": [
        "string"
      ],
      "contentRatingClass": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "embed": {},
      "hasAudio": true,
      "height": 1,
      "isPlayable": true,
      "language": "string",
      "license": "string",
      "link": "https://example.com",
      "metadata": {},
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pictures": {},
      "play": {},
      "playerEmbedUrl": "https://example.com",
      "privacy": {},
      "ratingModLocked": true,
      "releaseTime": "2026-05-07T12:00:00.000Z",
      "resourceKey": "string",
      "stats": {},
      "status": "string",
      "tags": [
        {}
      ],
      "transcode": {},
      "type": "string",
      "upload": {},
      "uploader": {},
      "uri": "string",
      "user": {},
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object | The originating Vimeo app information. |
| `categories` | array<object> | The categories associated with the video. |
| `contentRating` | array<string> | The content rating labels. |
| `contentRatingClass` | string | The normalized content rating classification. |
| `createdTime` | date | When the video was created. |
| `description` | string | The video description, when present. |
| `duration` | number | The video duration in seconds. |
| `embed` | object | The embed settings and iframe HTML. |
| `hasAudio` | boolean | Whether the video has audio. |
| `height` | number | The video height in pixels. |
| `isPlayable` | boolean | Whether the video is playable. |
| `language` | string | The video language, when present. |
| `license` | string | The video license, when present. |
| `link` | string | The public Vimeo URL for the video. |
| `metadata` | object | The video metadata connections and interactions. |
| `modifiedTime` | date | When the video was last modified. |
| `name` | string | The video name. |
| `pictures` | object | The video pictures object. |
| `play` | object | Playability details. |
| `playerEmbedUrl` | string | The embeddable player URL. |
| `privacy` | object | The video privacy settings. |
| `ratingModLocked` | boolean | Whether rating moderation is locked. |
| `releaseTime` | date | When the video was released. |
| `resourceKey` | string | The Vimeo resource key for the video. |
| `stats` | object | The video statistics object. |
| `status` | string | The video status. |
| `tags` | array<object> | The tags associated with the video. |
| `transcode` | object | Transcode details, when present. |
| `type` | string | The Vimeo resource type. |
| `upload` | object | Upload details, when present. |
| `uploader` | object | Uploader display information. |
| `uri` | string | The video URI. |
| `user` | object | The video owner. |
| `width` | number | The video width in pixels. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /channels/:channel_id/videos` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channel-videos.md) for the provider-specific parameters and requirements.

