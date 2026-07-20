# Vimeo: List Project Videos

Retrieves videos in a Vimeo project.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-project-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-project-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=152184&projectId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "152184",
  "projectId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-project-videos?${params}`, {
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
| `projectId` | number | yes | The ID of the folder. Example: `12345`. |
| `query` | string | no | The search query to use to filter the results. Example: `Stop motion`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | list<string> | no | The way to sort the results. One of: `alphabetical`, `date`, `default`, `duration`, `last_user_action_event_date`. Example: `date`. |
| `direction` | list<string> | no | The sort direction of the results. One of: `asc`, `desc`. Example: `asc`. |
| `filterTag` | string | no | A comma-separated list of tags to filter on. All results must include at least one of these tags. Accepts multiple values in one string, delimited by `,`. Example: `abc,xyz`. |
| `filterTagAllOf` | string | no | A comma-separated list of tags to filter on. All results must include all of these tags. Accepts multiple values in one string, delimited by `,`. Example: `abc,xyz`. |
| `filterTagExclude` | string | no | A comma-separated list of tags to exclude. Accepts multiple values in one string, delimited by `,`. Example: `abc,xyz`. |
| `queryFields` | string | no | A comma-separated list of fields to query over. Accepts multiple values in one string, delimited by `,`. Example: `title,description`. |
| `includeSubfolders` | boolean | no | Whether to include subfolders. Example: `false`. |

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

Through the native Vimeo API, this operation is `GET /users/:user_id/projects/:project_id/videos` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-videos.md) for the provider-specific parameters and requirements.

