# Vimeo: List Available Video Showcases

Retrieves showcases available for a Vimeo video.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-available-video-showcases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-available-video-showcases?connectionId=$CONNECTION_ID&limit=25&offset=0&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "videoId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-available-video-showcases?${params}`, {
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
| `videoId` | number | yes | The ID of the video. |
| `query` | string | no | Search text to filter the returned showcases. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "layout": "string",
      "link": "https://example.com",
      "metadata": {},
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pictures": {},
      "privacy": {},
      "resourceKey": "string",
      "shareLink": "https://example.com",
      "sort": "string",
      "theme": "string",
      "totalClips": 1,
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
| `createdTime` | date | When the showcase was created. |
| `description` | string | The showcase description. |
| `duration` | number | Total showcase duration in seconds. |
| `layout` | string | The showcase layout mode. |
| `link` | string | The public Vimeo showcase URL. |
| `metadata` | object | The showcase metadata connections and interactions. |
| `modifiedTime` | date | When the showcase was last modified. |
| `name` | string | The showcase name. |
| `pictures` | object | The showcase pictures object. |
| `privacy` | object | The showcase privacy settings. |
| `resourceKey` | string | The Vimeo resource key for the showcase. |
| `shareLink` | string | The share link for the showcase. |
| `sort` | string | The showcase sort mode. |
| `theme` | string | The showcase theme. |
| `totalClips` | number | Total number of clips in the showcase. |
| `uri` | string | The showcase API URI. |
| `user` | object | The showcase owner. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /videos/:video_id/available_albums` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-available-video-showcases.md) for the provider-specific parameters and requirements.

