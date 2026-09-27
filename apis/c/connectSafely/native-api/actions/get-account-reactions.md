# List an account's own reactions with ConnectSafely

Return a single page of the LinkedIn account's own reaction history (the posts this account reacted to), newest first. Lightweight — one LinkedIn call per request. To page, pass the returned `paginationToken` on the next request; keep going until `paginationToken` is null.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/:accountId/reactions`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [List an account's own reactions](https://connectsafely.ai/docs/api/linkedin-analytics/get-account-accountid-reactions-get-account-reactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | param | `string` | yes | LinkedIn account ID (24-character hex string) |
| `count` | query | `number` | no | Number of reactions to return per page Default: `20`. |
| `start` | query | `number` | no | Pagination offset (0-indexed). Ignored when paginationToken is provided. Default: `0`. |
| `paginationToken` | query | `string` | no | Token from a previous response to fetch the next page |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used |
| `profileId` | `string` | LinkedIn profile URN |
| `count` | `number` | Number of reactions returned in this page |
| `paginationToken` | `string` | Token for the next page; null when there are no more pages |
| `reactions` | `array` |  |
| `reactions[].activityUrn` | `string` | Activity URN of the reacted-to post |
| `reactions[].postUrl` | `string` | Permalink of the post that was reacted to (tracking params stripped) |
| `reactions[].reactionType` | `list` | Reaction the account applied — LIKE (👍), PRAISE (👏 Celebrate), APPRECIATION (❤️ Love), EMPATHY (🤝 Support), INTEREST (💡 Insightful), ENTERTAINMENT (😄 Funny). Null if the type could not be determined. |
| `reactions[].timestamp` | `number` | Reaction time (epoch ms) |
| `reactions[].isoDate` | `string` | Reaction time (ISO 8601) |
| `reactions[].type` | `list` |  |

### Example response

```json
{
  "success": true,
  "accountId": "6971843ca43920b1889fa28f",
  "profileId": "ACoAAFntzT4BELbT50_fDUyqwwNPXPXu-8P3HWc",
  "count": 1,
  "paginationToken": "dXJuOmxpOmFjdGl2aXR5Ojc0NzU1MzkxNzU0...",
  "reactions": [
    {
      "activityUrn": "7475545578450419712",
      "postUrl": "https://www.linkedin.com/posts/janedoe_growth-activity-7475545578450419712-abcd",
      "reactionType": "LIKE",
      "timestamp": 1782308954823,
      "isoDate": "2026-06-24 13:49:14.823000+00:00",
      "type": "reaction"
    }
  ]
}
```
