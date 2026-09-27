# Get the current user's LinkedIn home feed with ConnectSafely

Fetch posts from the authenticated user's LinkedIn home feed. Returns a mix of organic and promoted posts with author info, engagement metrics, and feed context (why the post appeared). Promoted posts are flagged with isPromoted: true.

## Endpoint

- **Method:** `POST`
- **Path:** `/feed`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get the current user's LinkedIn home feed](https://connectsafely.ai/docs/api/linkedin-posts/post-feed-get-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `count` | body | `number` | no | Number of feed posts to retrieve (max 50) Default: `5`. |
| `start` | body | `number` | no | Starting offset for pagination Default: `0`. |
| `sortOrder` | body | `list` | no | Feed sort order: relevance (default algorithm) or recent (newest first) Accepted values: `relevance`, `recent`. Default: `relevance`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `posts` | `array` |  |
| `posts[].activityUrn` | `string` | LinkedIn activity URN of the post |
| `posts[].postUrl` | `string` | Direct URL to the post |
| `posts[].author` | `object` |  |
| `posts[].author.name` | `string` | Author display name |
| `posts[].author.profileUrl` | `string` | Author profile or company URL |
| `posts[].author.profileId` | `string` | Author vanity name or company slug |
| `posts[].author.headline` | `string` | Author professional headline |
| `posts[].author.connectionDegree` | `string` | Connection degree (1st, 2nd, 3rd+, Following) |
| `posts[].author.isPremium` | `boolean` | Whether the author has a Premium badge |
| `posts[].author.isCompany` | `boolean` | Whether the author is a company/organization |
| `posts[].content` | `string` | Post text content |
| `posts[].timestamp` | `string` | Relative timestamp (e.g., "5h", "3d", "1w") |
| `posts[].engagement` | `object` |  |
| `posts[].engagement.reactions` | `number` | Total reaction count |
| `posts[].engagement.comments` | `number` | Comment count |
| `posts[].engagement.reposts` | `number` | Repost count |
| `posts[].hashtags` | `array` | Hashtags extracted from the post content |
| `posts[].isPromoted` | `boolean` | Whether this is a promoted/sponsored post |
| `posts[].feedContext` | `string` | Why this post appeared in the feed (e.g., "Suggested", "John commented on this") |
| `count` | `number` | Number of posts returned |

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
