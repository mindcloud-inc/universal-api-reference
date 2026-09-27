# Get reactions from a post (v2 - with vanity names) with ConnectSafely

Retrieve reactions from a LinkedIn post. Returns vanity names (actorPublicIdentifier) and proper profile URLs. Identical to /posts/reactions — pages by token like /posts/comments: pass the previous response's pagination.nextPaginationToken back as paginationToken.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/reactions/v2`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get reactions from a post (v2 - with vanity names)](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-reactions-v2-get-post-reactions-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `postUrl` | body | `string` | yes | Full URL of the LinkedIn post to get reactions from |
| `count` | body | `number` | no | Number of reactions per page (default 10) |
| `paginationToken` | body | `string` | no | Token from previous response to fetch next page |
| `pageToken` | body | `string` | no | Deprecated alias for paginationToken, kept for existing v2 clients |
| `start` | body | `number` | no | Deprecated. LinkedIn pages this endpoint by token only, so this value is ignored. Use paginationToken. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `postUrl` | `string` | URL of the post |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `reactions` | `array` |  |
| `reactions[].actorUrn` | `string` | URN of the person who reacted (null in v2) |
| `reactions[].postUrn` | `string` | URN of the post |
| `reactions[].reactionType` | `string` | Type of reaction (LIKE, PRAISE, APPRECIATION, EMPATHY, INTEREST, ENTERTAINMENT) |
| `reactions[].actorType` | `string` | Type of actor (profile) |
| `reactions[].actorName` | `string` | Name of the person who reacted |
| `reactions[].actorHeadline` | `string` | Headline of the person who reacted |
| `reactions[].actorPublicIdentifier` | `string` | Vanity name / public identifier (e.g. john-doe-123) |
| `reactions[].actorProfilePicture` | `string` | URL to profile picture |
| `reactions[].actorProfileUrl` | `string` | Full URL to the profile (linkedin.com/in/vanityName) |
| `reactions[].connectionDegree` | `string` | Connection degree (1st, 2nd, 3rd+) |
| `pagination` | `object` |  |
| `pagination.count` | `number` | Number of reactions in this page |
| `pagination.hasNextPage` | `boolean` | True when LinkedIn handed back a token for another page |
| `pagination.nextPaginationToken` | `string` | Pass back as paginationToken to fetch the next page |
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
  "postUrl": "https://www.linkedin.com/feed/update/urn:li:activity:7430667226199830528/",
  "accountId": "696ce9e780e0483585e4e553",
  "reactions": [
    {
      "actorUrn": null,
      "postUrn": "urn:li:activity:7430667226199830528",
      "reactionType": "LIKE",
      "actorType": "profile",
      "actorName": "John Doe",
      "actorHeadline": "Software Engineer at Tech Company",
      "actorPublicIdentifier": "john-doe-123",
      "actorProfilePicture": "https://media.licdn.com/dms/image/...",
      "actorProfileUrl": "https://www.linkedin.com/in/john-doe-123/",
      "connectionDegree": "1st"
    }
  ],
  "pagination": {
    "count": 10,
    "hasNextPage": true,
    "nextPaginationToken": "CiAyMDhhZjk1Y2E4MDE5YWQwNDI2ZTZhZTJhNTM2NzkzMBAK"
  },
  "postDetails": {
    "activityUrn": "urn:li:activity:7430667226199830528",
    "ugcPostUrn": null,
    "shareUrn": "urn:li:share:7430667225633550337",
    "featuredActivityUrn": null,
    "content": "Post content here..."
  }
}
```

## Error status codes

`400`, `401`. Bodies follow the shared `{ success, code, message }` error shape.
