# React to a LinkedIn post with ConnectSafely

Add a reaction to a LinkedIn post. LinkedIn supports 6 reaction types beyond simple likes. Reactions are a lightweight way to engage with content and increase visibility in your network. Supports reacting as a company page if you have admin access.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/react`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [React to a LinkedIn post](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-react-react-to-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `postUrl` | body | `string` | yes | Full URL of the LinkedIn post to react to. Can also provide threadUrn directly instead. |
| `threadUrn` | body | `string` | no | Thread URN of the post. If provided, skips URL scraping for faster execution. |
| `reactionType` | body | `list` | no | Reaction type: LIKE (thumbs up), PRAISE (clap), APPRECIATION (heart), EMPATHY (caring), INTEREST (insightful), ENTERTAINMENT (funny) Accepted values: `LIKE`, `PRAISE`, `APPRECIATION`, `EMPATHY`, `INTEREST`, `ENTERTAINMENT`. Default: `LIKE`. |
| `companyUrn` | body | `string` | no | Company URN to react as company page instead of personal profile (e.g., "urn:li:fsd_company:123456"). Requires admin access to the company page. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` | Success message describing the action |
| `postUrl` | `string` | URL of the post that was reacted to |
| `threadUrn` | `string` | Thread URN of the post |
| `reactionType` | `string` | Type of reaction applied (LIKE, PRAISE, etc.) |
| `accountId` | `string` | LinkedIn account ID that added the reaction |
| `companyUrn` | `string` | Company URN if reacted as company page |
| `postDetails` | `object` | Details about the post that was reacted to |
| `postDetails.activityUrn` | `string` | Activity URN of the post |
| `postDetails.ugcPostUrn` | `string` | UGC Post URN if available |
| `postDetails.shareUrn` | `string` | Share URN of the post |
| `postDetails.featuredActivityUrn` | `string` | Featured activity URN if applicable |
| `postDetails.content` | `string` | Content/text of the original post |

### Example response

```json
{
  "success": true,
  "message": "Successfully reacted to post with LIKE reaction",
  "postUrl": "https://www.linkedin.com/feed/update/urn:li:activity:7430667226199830528/",
  "threadUrn": "urn:li:activity:7430667226199830528",
  "reactionType": "LIKE",
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

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
