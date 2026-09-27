# Get latest posts from a profile with ConnectSafely

Retrieve the most recent posts from a LinkedIn profile. Useful for monitoring competitor content, tracking influencer activity, or finding engagement opportunities. Can include or exclude reposts/shares.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/latest`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get latest posts from a profile](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-latest-get-latest-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | body | `string` | no | LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123"). When possible, use profileUrn instead for more reliable results. |
| `profileUrn` | body | `string` | no | LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over profileId — avoids an extra API call to resolve the vanity name. |
| `count` | body | `number` | no | Number of recent posts to retrieve (max 20) Default: `1`. |
| `includeReposts` | body | `boolean` | no | Whether to include reposts/shares in results Default: `True`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `profileUrn` | `string` | LinkedIn profile URN of the target user |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `posts` | `array` |  |
| `posts[].activityUrn` | `string` | LinkedIn activity URN of the post |
| `posts[].url` | `string` | Direct URL to the LinkedIn post |
| `posts[].content` | `string` | Post text content (commentary) |
| `posts[].isGroupPost` | `boolean` | Whether this post is from a LinkedIn group |
| `posts[].numLikes` | `number` | Number of likes/reactions on the post |
| `posts[].numComments` | `number` | Number of comments on the post |
| `posts[].numShares` | `number` | Number of shares/reposts of this post |
| `posts[].authorName` | `string` | Name of the post author |
| `posts[].authorProfileUrl` | `string` | LinkedIn profile URL of the author |
| `posts[].authorProfilePicture` | `string` | Profile picture URL of the author |
| `posts[].authorType` | `list` | Type of author (person or company) |
| `posts[].isEdited` | `boolean` | Whether the post has been edited |
| `posts[].isArticle` | `boolean` | Whether the post is an article |
| `posts[].isRepost` | `boolean` | Whether the post is a repost/reshare |
| `posts[].timestamp` | `string` | Relative timestamp of the post (e.g., "1w", "3d") |
| `count` | `number` | Number of posts requested |
| `totalPostsFound` | `number` | Total number of posts found and returned |
| `message` | `string` | Status message describing the result |

### Example response

```json
{
  "success": true,
  "profileUrn": "urn:li:fsd_profile:ACoAAA24A-MBVEvT49xpVF2gnWrhvmUIPDJshSM",
  "accountId": "696ce9e780e0483585e4e553",
  "posts": [
    {
      "activityUrn": "urn:li:activity:7429892659739029504",
      "url": "https://www.linkedin.com/feed/update/urn:li:activity:7429892659739029504",
      "content": "The end of Q1. And what a three months it's been...",
      "isGroupPost": false,
      "numLikes": 86,
      "numComments": 5,
      "numShares": 2,
      "authorName": "Andy Burrows",
      "authorProfileUrl": "https://www.linkedin.com/in/andy-burrows-60256731",
      "authorProfilePicture": "https://media.licdn.com/dms/image/...",
      "authorType": "person",
      "isEdited": false,
      "isArticle": false,
      "isRepost": false,
      "timestamp": "1w"
    }
  ],
  "count": 1,
  "totalPostsFound": 1,
  "message": "Found 1 valid posts out of 1 total posts"
}
```

## Error status codes

`400`, `401`, `404`. Bodies follow the shared `{ success, code, message }` error shape.
