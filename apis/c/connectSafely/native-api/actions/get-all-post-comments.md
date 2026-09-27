# Get all comments from a post with ConnectSafely

Fetch all comments from a LinkedIn post in a single request. Automatically handles pagination internally. Ideal for bulk analysis of post engagement. Use for posts with many comments where you need complete data.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/comments/all`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get all comments from a post](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-comments-all-get-all-post-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `postUrl` | body | `string` | yes | Full URL of the LinkedIn post to get all comments from |
| `batchSize` | body | `number` | no | Number of comments to fetch per internal request Default: `50`. |
| `maxComments` | body | `number` | no | Maximum total comments to retrieve (safety limit) Default: `1000`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `postUrl` | `string` | URL of the post |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `comments` | `array` |  |
| `comments[].commentId` | `string` |  |
| `comments[].authorName` | `string` |  |
| `comments[].commentText` | `string` |  |
| `comments[].authorDesignation` | `string` |  |
| `comments[].commenterProfileId` | `string` |  |
| `comments[].publicIdentifier` | `string` |  |
| `comments[].profileUrl` | `string` |  |
| `comments[].authorProfilePicture` | `string` |  |
| `comments[].createdAt` | `number` |  |
| `comments[].likeCount` | `number` |  |
| `comments[].replyCount` | `number` |  |
| `comments[].hasProfile` | `boolean` |  |
| `comments[].commenterUrn` | `string` |  |
| `summary` | `object` | Summary of the fetch operation |
| `summary.totalComments` | `number` | Total number of comments fetched |
| `summary.fetchDurationMs` | `number` | Time taken to fetch all comments in milliseconds |
| `summary.maxCommentsLimit` | `number` | Maximum comments limit configured |
| `summary.batchSize` | `number` | Batch size used for fetching |
| `summary.truncated` | `boolean` | Whether results were truncated due to limit |
| `postDetails` | `object` |  |
| `postDetails.activityUrn` | `string` |  |
| `postDetails.ugcPostUrn` | `string` |  |
| `postDetails.shareUrn` | `string` |  |
| `postDetails.featuredActivityUrn` | `string` |  |
| `postDetails.content` | `string` |  |

### Example response

```json
{
  "success": true,
  "postUrl": "https://www.linkedin.com/feed/update/urn:li:activity:7431898703118110720",
  "accountId": "696ce9e780e0483585e4e553",
  "comments": [
    {
      "commentId": "urn:li:fsd_comment:(7431913248658059265,urn:li:ugcPost:7431898701888966656)",
      "authorName": "John Doe",
      "commentText": "Great post!",
      "authorDesignation": "Engineer",
      "commenterProfileId": "ACoAAA...",
      "publicIdentifier": "john-doe",
      "profileUrl": "https://www.linkedin.com/in/john-doe",
      "authorProfilePicture": "https://media.licdn.com/...",
      "createdAt": 1771906196752,
      "likeCount": 3,
      "replyCount": 1,
      "hasProfile": true,
      "commenterUrn": "urn:li:fsd_profile:ACoAAA..."
    }
  ],
  "summary": {
    "totalComments": 15,
    "fetchDurationMs": 4253,
    "maxCommentsLimit": 1000,
    "batchSize": 50,
    "truncated": false
  },
  "postDetails": {
    "activityUrn": "urn:li:activity:7431898703118110720",
    "ugcPostUrn": "urn:li:ugcPost:7431898701888966656",
    "shareUrn": null,
    "featuredActivityUrn": null,
    "content": "Post content here..."
  }
}
```

## Error status codes

`400`, `401`. Bodies follow the shared `{ success, code, message }` error shape.
