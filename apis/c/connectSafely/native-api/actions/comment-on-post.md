# Comment on a LinkedIn post with ConnectSafely

Add a comment to a LinkedIn post. Comments increase engagement and visibility. Set `tagPostAuthor` to true to tag the post author with a real @mention that notifies them. Supports posting as a company page if you have admin access. **Rate limit: 100 comments per day.**

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/comment`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Comment on a LinkedIn post](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-comment-comment-on-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `postUrl` | body | `string` | yes | Full URL of the LinkedIn post to comment on |
| `comment` | body | `string` | yes | Comment text content. Supports @mentions and hashtags. When `tagPostAuthor` is true, place a {{author}} placeholder where the author tag should appear — otherwise the author name is prepended. |
| `tagPostAuthor` | body | `boolean` | no | When true, tags the post author with a real @mention that notifies them. The tag is inserted at a {{author}} placeholder in `comment` if present, otherwise the author name is prepended. Default: `False`. |
| `companyUrn` | body | `string` | no | Company URN to post comment as company page instead of personal profile |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` | Success message |
| `postUrl` | `string` | URL of the post that was commented on |
| `comment` | `string` | The comment text that was posted |
| `accountId` | `string` | LinkedIn account ID that posted the comment |
| `postDetails` | `object` | Details about the post that was commented on |
| `postDetails.activityUrn` | `string` | Activity URN of the post |
| `postDetails.ugcPostUrn` | `string` | UGC Post URN if available |
| `postDetails.shareUrn` | `string` | Share URN of the post |
| `postDetails.featuredActivityUrn` | `string` | Featured activity URN if applicable |
| `postDetails.content` | `string` | Content/text of the original post |

### Example response

```json
{
  "success": true,
  "message": "Successfully posted comment",
  "postUrl": "https://www.linkedin.com/feed/update/urn:li:activity:7430667226199830528/",
  "comment": "Great insights! Thanks for sharing.",
  "accountId": "696ce9e780e0483585e4e553",
  "postDetails": {
    "activityUrn": "urn:li:activity:7430667226199830528",
    "ugcPostUrn": null,
    "shareUrn": "urn:li:share:7430667225633550337",
    "featuredActivityUrn": null,
    "content": "Discover proven LinkedIn strategies for consultants to attract high-value clients..."
  }
}
```

## Error status codes

`400`, `401`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
