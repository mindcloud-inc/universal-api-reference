# Vimeo: List Video Comments

Retrieves comments on a Vimeo video.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-video-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-video-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&videoId=247950140" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "videoId": "247950140"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-video-comments?${params}`, {
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
| `videoId` | number | yes | The ID of the video. Example: `247950140`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `direction` | list | no | The sort direction of the results. One of: `asc`, `desc`. Example: `asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "deletedOn": "2026-05-07T12:00:00.000Z",
      "lastEditedOn": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com",
      "metadata": {},
      "text": "string",
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
| `createdOn` | date | Comment creation time. |
| `deletedOn` | date | Comment deletion time. |
| `lastEditedOn` | date | Comment last edit time. |
| `link` | string | Comment permalink. |
| `metadata` | object | Comment metadata. |
| `text` | string | Comment text. |
| `uri` | string | Comment URI. |
| `user` | object | Comment author. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /videos/:video_id/comments` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-video-comments.md) for the provider-specific parameters and requirements.

