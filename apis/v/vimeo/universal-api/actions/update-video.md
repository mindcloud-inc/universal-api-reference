# Vimeo: Update Video

Updates an existing video in Vimeo.

```
PUT https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/update-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/update-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "1146062919"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/update-video', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "1146062919"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | number | yes | The ID of the video. Example: `1146062919`. |
| `name` | string | no | The title of the video. This field can hold a maximum of 128 characters. Example: `Behind the scenes of Vimeo's Short Film Grant Program`. |
| `customUrl` | string | no | The custom link of the video. Example: `puppies`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The description of the video. This field can hold a maximum of 5000 characters. Example: `A celebration of 10 years of Staff Picks.`. |
| `privacy.view` | list | no | The video's privacy setting. One of: `anybody`, `contacts`, `disable`, `nobody`, `password`, `team`, `unlisted`, `users`. Example: `unlisted`. |
| `contentRating[]` | array<string> | no | A list of values describing the content in this video. |
| `hideFromVimeo` | boolean | no | Whether to hide the video from everyone except the video's owner. Example: `false`. |
| `license` | list | no | The Creative Commons license under which the video is offered. One of: `by`, `by-nc`, `by-nc-nd`, `by-nc-sa`, `by-nd`, `by-sa`, `cc0`. |
| `locale` | string | no | The video's default language. Example: `en-US`. |
| `privacy.add` | boolean | no | Whether a user can add the video to a showcase, channel, or group. Example: `true`. |
| `privacy.comments` | list | no | The privacy level required to comment on the video. One of: `anybody`, `contacts`, `nobody`. |
| `privacy.download` | boolean | no | Whether a user can download the video. Example: `true`. |
| `privacy.embed` | list | no | The video's embed setting. One of: `private`, `public`, `whitelist`. |
| `reviewPage.active` | boolean | no | Whether to enable video review. Example: `true`. |

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

Through the native Vimeo API, this operation is `PATCH /videos/:video_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video.md) for the provider-specific parameters and requirements.

