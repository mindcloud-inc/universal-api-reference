# Vimeo: List User Videos

Retrieves a user's uploaded videos from Vimeo.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-user-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-user-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=152184" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "152184"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-user-videos?${params}`, {
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
| `query` | string | no | The search query to use to filter the results. Example: `Vimeo`. |
| `filter` | list | no | The attribute by which to filter the results. One of: `app_only`, `cold_storage`, `embeddable`, `featured`, `live`, `no_placeholder`, `nolive`, `playable`, `screen_recorded`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queryFields` | list | no | The fields to search against. One of: `chapters`, `description`, `tags`, `title`. Accepts multiple values in one string. |
| `containingUri` | string | no | Return only videos that contain the specified URI. Example: `/users/152184/videos/258684937`. |
| `filterTag` | string | no | Return only videos with the specified tag. Example: `staff-picks`. |
| `filterTagAllOf` | string | no | Return only videos that contain all specified tags. Example: `staff-picks,featured`. |
| `filterTagExclude` | string | no | Return only videos that exclude the specified tag. Example: `staff-picks`. |
| `filterUploader` | number | no | Return only videos uploaded by the specified uploader ID. Example: `152184`. |
| `filterEmbeddable` | boolean | no | Whether to filter by embeddable videos. Example: `true`. |
| `filterPlayable` | boolean | no | Whether to filter by playable videos. Example: `true`. |
| `filterScreenRecorded` | boolean | no | Whether to filter by screen-recorded videos. Example: `true`. |

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

Through the native Vimeo API, this operation is `GET /users/:user_id/videos` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-videos.md) for the provider-specific parameters and requirements.

