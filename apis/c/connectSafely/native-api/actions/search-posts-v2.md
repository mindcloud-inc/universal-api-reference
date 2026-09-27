# Search LinkedIn posts (V2 - with auto-pagination) with ConnectSafely

Search for LinkedIn posts with enhanced filtering options and automatic pagination. Automatically handles LinkedIn pagination internally - specify the total count you want (max 50) and the API will fetch multiple pages as needed (max 10 pages, 10 results per page). Supports filtering by date, content type, author, and more.

**Important:** This V2 endpoint uses LinkedIn's newer search, which is rolling out gradually by region. If this endpoint does not return results for your account, use the V1 `/search/posts` endpoint instead.

**Rate limit:** 1,000 search calls per account per day (resets at midnight UTC), and 30 calls per minute. One request counts as one call regardless of `count`.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/posts/v2`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search LinkedIn posts (V2 - with auto-pagination)](https://connectsafely.ai/docs/api/linkedin-search/post-search-posts-v2-search-posts-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `keywords` | body | `string` | no | Search keywords for post content Default: ``. |
| `count` | body | `number` | no | Total number of posts to return. API will automatically paginate (10 per page) to collect this many. Default: `10`. |
| `start` | body | `number` | no | Starting offset (0-indexed) for pagination. Default: `0`. |
| `exactSearch` | body | `boolean` | no | When true (default), the keyword is wrapped in double quotes for an exact-phrase match. Set to false for a broader search that also matches individual terms. Default: `True`. |
| `filters` | body | `object` | no | Optional filters to narrow down search results |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `posts` | `array` |  |
| `posts[].postUrl` | `string` |  |
| `posts[].authorName` | `string` |  |
| `posts[].authorProfileUrl` | `string` |  |
| `posts[].content` | `string` |  |
| `posts[].timestamp` | `string` | Relative time string (e.g., "3mo", "2w", "1d") |
| `posts[].likes` | `number` |  |
| `posts[].comments` | `number` |  |
| `posts[].shares` | `number` |  |
| `posts[].isPeopleUpdate` | `boolean` | True if this is a people update post (job change, promotion, work anniversary, etc.) |
| `posts[].celebrationType` | `string` | Type of celebration/update (e.g., "Starting a new position", "Got promoted", "Work anniversary") |
| `posts[].isArticle` | `boolean` | True if this is a collaborative article (pulse URL) |
| `posts[].articleUrl` | `string` | Article URL for collaborative articles |
| `posts[].canComment` | `boolean` | False if commenting is disabled (e.g., for collaborative articles) |
| `count` | `number` | Number of posts returned in this response |
| `totalCount` | `number` | Total number of matching results available on LinkedIn (may be 0 if unknown) |

### Example response

```json
{
  "success": true,
  "posts": [
    {
      "activityUrn": "urn:li:ugcPost:7431688584019111936",
      "postUrl": "https://www.linkedin.com/feed/update/urn:li:ugcPost:7431688584019111936/",
      "author": {
        "profileId": "shiv-pandya-2ab25817",
        "profileUrl": "https://www.linkedin.com/in/shiv-pandya-2ab25817/",
        "name": "Shiv Pandya",
        "headline": "Business Head- Kashyap Solar (Renewable Energy)",
        "profilePicture": "",
        "connectionDegree": "2nd",
        "isVerified": false,
        "isPremium": false
      },
      "content": "AI (Artificial intelligence) is rapidly transforming major industries...",
      "timestamp": "1d",
      "visibility": "public",
      "engagement": {
        "reactions": 12,
        "comments": 2,
        "reposts": 0
      },
      "hashtags": [
        "#solar",
        "#AI",
        "#power"
      ],
      "isPeopleUpdate": false,
      "isArticle": false,
      "canComment": true
    }
  ],
  "count": 3,
  "totalCount": 0
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
