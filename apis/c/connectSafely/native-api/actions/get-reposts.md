# Get the list of people who reposted a post with ConnectSafely

Retrieve the list of people who reposted a LinkedIn post. Returns each reposter's name, vanity name (actorPublicIdentifier), profile URL and profile picture, plus a repostType ("simple" = plain repost, "quote" = repost with commentary). Uses cursor-based pagination: pass the returned pagination.token together with nextStartIndex to fetch the next page.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/reposts`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get the list of people who reposted a post](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-reposts-get-reposts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `postUrl` | body | `string` | yes | Full URL of the LinkedIn post to get reposters from |
| `count` | body | `number` | no | Number of reposters to request per page (default 50) |
| `startIndex` | body | `number` | no | Offset for pagination (default 0). Use pagination.nextStartIndex from the previous response. |
| `token` | body | `string` | no | Cursor token from a previous response (pagination.token). Required together with startIndex for subsequent pages. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `postUrl` | `string` | URL of the post |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `reposters` | `array` |  |
| `reposters[].actorType` | `string` | Type of actor (profile, company). A company page can repost as itself. |
| `reposters[].actorName` | `string` | Name of the person or company page that reposted |
| `reposters[].actorPublicIdentifier` | `string` | Vanity name / public identifier — the member vanity for a profile (e.g. himansuuverma), the company universal name for a company (e.g. multioutreachagency) |
| `reposters[].actorProfilePicture` | `string` | URL to profile picture |
| `reposters[].actorProfileUrl` | `string` | Full URL to the profile (linkedin.com/in/vanityName) |
| `reposters[].repostType` | `list` | "simple" = plain repost, "quote" = repost with commentary |
| `pagination` | `object` |  |
| `pagination.startIndex` | `number` |  |
| `pagination.count` | `number` | Number of reposters returned on this page |
| `pagination.hasNextPage` | `boolean` |  |
| `pagination.nextStartIndex` | `number` | Pass as startIndex (with token) to fetch the next page |
| `pagination.token` | `string` | Cursor token for next page. Pass as token (with nextStartIndex as startIndex) in next request. |
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
  "postUrl": "https://www.linkedin.com/feed/update/urn:li:activity:7468554531233185792/",
  "accountId": "696ce9e780e0483585e4e553",
  "reposters": [
    {
      "actorType": "profile",
      "actorName": "Himanshu Verma",
      "actorPublicIdentifier": "himansuuverma",
      "actorProfilePicture": "https://media.licdn.com/dms/image/...",
      "actorProfileUrl": "https://www.linkedin.com/in/himansuuverma",
      "repostType": "simple"
    }
  ],
  "pagination": {
    "startIndex": 0,
    "count": 10,
    "hasNextPage": true,
    "nextStartIndex": 10,
    "token": "Cjc4MDcxMjk3My0xNzgwOTg1MTY1OTk0LTVmNmY2NzMzMzZjZTg0ZjA1MzExMGU4ZDdmZGUwYTdl"
  },
  "postDetails": {
    "activityUrn": "urn:li:activity:7468554531233185792",
    "ugcPostUrn": null,
    "shareUrn": "urn:li:share:7468554530276720640",
    "featuredActivityUrn": null,
    "content": "Claude just became a Wall Street analyst..."
  }
}
```

## Error status codes

`400`, `401`. Bodies follow the shared `{ success, code, message }` error shape.
