# Vimeo: List Comment Replies

Retrieves replies to a Vimeo video comment.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-comment-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-comment-replies?connectionId=$CONNECTION_ID&limit=25&offset=0&videoId=1&commentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "videoId": "1",
  "commentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-comment-replies?${params}`, {
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
| `commentId` | number | yes | The ID of the comment. |

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
      "resourceKey": "string",
      "text": "string",
      "type": "string",
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
| `createdOn` | date | When the reply was created. |
| `deletedOn` | date | When the reply was deleted, when present. |
| `lastEditedOn` | date | When the reply was last edited, when present. |
| `link` | string | The public Vimeo URL for the reply. |
| `metadata` | object | The reply metadata connections and interactions. |
| `resourceKey` | string | The Vimeo resource key for the reply. |
| `text` | string | The reply text. |
| `type` | string | The Vimeo resource type. |
| `uri` | string | The reply URI. |
| `user` | object | The user who wrote the reply. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /videos/:video_id/comments/:comment_id/replies` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comment-replies.md) for the provider-specific parameters and requirements.

