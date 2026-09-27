# Like a comment with ConnectSafely

Like an existing comment on a LinkedIn post. Sends a pre-signal to LinkedIn before the actual like action for realistic engagement simulation.

## Endpoint

- **Method:** `POST`
- **Path:** `/like-comment`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Like a comment](https://connectsafely.ai/docs/api/linkedin-posts/post-like-comment-like-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `commentId` | body | `string` | yes | ID of the comment to like (same format as used in reply endpoint, from /posts/comments response) |
| `postUrl` | body | `string` | no | Optional post URL for referer header (helps with browser simulation) |
| `companyUrn` | body | `string` | no | Optional company URN if liking as a company page |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `commentId` | `string` |  |
| `originalCommentId` | `string` |  |
| `accountId` | `string` |  |

### Example response

```json
{
  "success": true,
  "message": "Successfully liked comment",
  "commentId": "urn:li:comment:(activity:7441028442856251392,7441783492948054016)",
  "originalCommentId": "7441783492948054016",
  "accountId": "acc_123"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
