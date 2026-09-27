# Get comments from a post with ConnectSafely

Retrieve comments from a LinkedIn post with pagination support. Useful for analyzing engagement, finding leads who commented, or monitoring discussions. Returns comment content, author info, timestamps, and like counts.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/comments`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get comments from a post](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-comments-get-post-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `postUrl` | body | `string` | yes | Full URL of the LinkedIn post to get comments from |
| `commentCount` | body | `number` | no | Number of comments per page (enables pagination mode) |
| `start` | body | `number` | no | Pagination offset (0-indexed) |
| `paginationToken` | body | `string` | no | Token from previous response to fetch next page |
| `maxComments` | body | `number` | no | Maximum total comments to retrieve Default: `1000`. |
| `batchSize` | body | `number` | no | Internal batch size for fetching Default: `50`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `postUrl` | `string` | URL of the post |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `comments` | `array` |  |
| `comments[].commentId` | `string` | Unique identifier for the comment |
| `comments[].authorName` | `string` | Name of the comment author |
| `comments[].commentText` | `string` | Content of the comment |
| `comments[].authorDesignation` | `string` | Headline/designation of the author |
| `comments[].commenterProfileId` | `string` | Profile URN of the commenter |
| `comments[].publicIdentifier` | `string` | Public ID for the profile URL |
| `comments[].profileUrl` | `string` | Full URL to the commenter profile |
| `comments[].authorProfilePicture` | `string` | URL to profile picture |
| `comments[].createdAt` | `number` | Timestamp when comment was created |
| `comments[].likeCount` | `number` | Number of likes on the comment |
| `comments[].replyCount` | `number` | Number of replies to the comment |
| `comments[].hasProfile` | `boolean` | Whether commenter has a profile |
| `comments[].commenterUrn` | `string` | URN of the commenter |
| `pagination` | `object` |  |
| `pagination.start` | `number` |  |
| `pagination.count` | `number` |  |
| `pagination.total` | `number` |  |
| `pagination.hasNextPage` | `boolean` |  |
| `pagination.nextPaginationToken` | `string` |  |
| `pagination.nextStart` | `number` |  |
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
      "commentText": "Great insights! Thanks for sharing.",
      "authorDesignation": "Software Engineer at Tech Company",
      "commenterProfileId": "ACoAAAkEZoAB2YcQrbVMuMkEvlMH8zSEC5ESxec",
      "publicIdentifier": "john-doe-123",
      "profileUrl": "https://www.linkedin.com/in/john-doe-123",
      "authorProfilePicture": "https://media.licdn.com/dms/image/...",
      "createdAt": 1771906196752,
      "likeCount": 5,
      "replyCount": 2,
      "hasProfile": true,
      "commenterUrn": "urn:li:fsd_profile:ACoAAAkEZoAB2YcQrbVMuMkEvlMH8zSEC5ESxec"
    }
  ],
  "pagination": {
    "start": 0,
    "count": 5,
    "total": 10,
    "hasNextPage": true,
    "nextPaginationToken": "abc123",
    "nextStart": 5
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
