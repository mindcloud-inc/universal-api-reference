# BlogIn: Delete Post Comment

Deletes a comment from a BlogIn post.

```
DELETE https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/delete-post-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/delete-post-comment?connectionId=$CONNECTION_ID&postId=1&commentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "1",
  "commentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/delete-post-comment?${params}`, {
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
| `postId` | number | yes | The ID of the parent post. |
| `commentId` | number | yes | The ID of the comment to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlogIn API returns.

## Native endpoint

Through the native BlogIn API, this operation is `DELETE /posts/:postId/comments/:commentId` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post-comment.md) for the provider-specific parameters and requirements.

