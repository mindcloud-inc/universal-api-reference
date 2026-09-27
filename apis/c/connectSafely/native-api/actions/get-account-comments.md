# List an account's own comments with ConnectSafely

Return a single page of the LinkedIn account's own comment history (the comments this account left on posts), newest first. Lightweight — one LinkedIn call per request. To page, pass the returned `paginationToken` on the next request; keep going until `paginationToken` is null.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/:accountId/comments`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [List an account's own comments](https://connectsafely.ai/docs/api/linkedin-analytics/get-account-accountid-comments-get-account-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | param | `string` | yes | LinkedIn account ID (24-character hex string) |
| `count` | query | `number` | no | Number of comments to return per page Default: `20`. |
| `start` | query | `number` | no | Pagination offset (0-indexed). Ignored when paginationToken is provided. Default: `0`. |
| `paginationToken` | query | `string` | no | Token from a previous response to fetch the next page |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used |
| `profileId` | `string` | LinkedIn profile URN |
| `count` | `number` | Number of comments returned in this page |
| `paginationToken` | `string` | Token for the next page; null when there are no more pages |
| `comments` | `array` |  |
| `comments[].activityUrn` | `string` | Internal update/activity URN for this comment item |
| `comments[].postActivityUrn` | `string` | Numeric activity id of the post that was commented on |
| `comments[].commentUrn` | `string` | URN of the account's comment |
| `comments[].commentText` | `string` | Text of the comment the account left (null if not exposed) |
| `comments[].postUrl` | `string` | Permalink of the post that was commented on (null if not exposed) |
| `comments[].timestamp` | `number` | Comment time (epoch ms) |
| `comments[].isoDate` | `string` | Comment time (ISO 8601) |
| `comments[].type` | `list` |  |

### Example response

```json
{
  "success": true,
  "accountId": "6971843ca43920b1889fa28f",
  "profileId": "ACoAAFntzT4BELbT50_fDUyqwwNPXPXu-8P3HWc",
  "count": 1,
  "paginationToken": "dXJuOmxpOmFjdGl2aXR5Ojc0NzQ5NzY5OTU3...",
  "comments": [
    {
      "activityUrn": "7475780581708955648",
      "postActivityUrn": "7475769998100099073",
      "commentUrn": "urn:li:fsd_comment:(7475777250785914880,urn:li:activity:7475769998100099073)",
      "commentText": "This is awesome to see \ud83d\ude00",
      "postUrl": "https://www.linkedin.com/posts/karan-kumar-62b763103_linkedingrowth-inboundleads-saas-activity-7475769998100099073-AHix",
      "timestamp": 1782308004423,
      "isoDate": "2026-06-24 13:33:24.423000+00:00",
      "type": "comment"
    }
  ]
}
```
