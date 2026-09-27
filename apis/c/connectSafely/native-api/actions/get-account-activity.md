# Get account activity history with ConnectSafely

Retrieve activity history for the last 15 days including comments and reactions. Returns summary statistics, daily breakdown, and individual activity records. Useful for tracking account behavior, auditing actions, and monitoring engagement patterns.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/:accountId/activity`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get account activity history](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-activity-get-account-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | param | `string` | yes | Unique identifier for the LinkedIn account (24-character hex string) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` |  |
| `accountName` | `string` |  |
| `dateRange` | `object` |  |
| `dateRange.start` | `date` |  |
| `dateRange.end` | `date` |  |
| `dateRange.days` | `number` |  |
| `summary` | `object` |  |
| `summary.totalComments` | `number` |  |
| `summary.totalReactions` | `number` |  |
| `summary.totalActivities` | `number` |  |
| `summary.totalCommentsFetched` | `number` |  |
| `summary.totalReactionsFetched` | `number` |  |
| `summary.reachedCommentLimit` | `boolean` |  |
| `summary.reachedReactionLimit` | `boolean` |  |
| `dailyBreakdown` | `array` |  |
| `dailyBreakdown[].date` | `string` |  |
| `dailyBreakdown[].comments` | `number` |  |
| `dailyBreakdown[].reactions` | `number` |  |
| `dailyBreakdown[].total` | `number` |  |
| `comments` | `array` |  |
| `comments[].activityUrn` | `string` |  |
| `comments[].date` | `string` |  |
| `comments[].isoDate` | `date` |  |
| `comments[].timestamp` | `number` |  |
| `comments[].type` | `list` |  |
| `reactions` | `array` |  |
| `reactions[].activityUrn` | `string` |  |
| `reactions[].date` | `string` |  |
| `reactions[].isoDate` | `date` |  |
| `reactions[].timestamp` | `number` |  |
| `reactions[].type` | `list` |  |

## Error status codes

`400`, `401`, `404`. Bodies follow the shared `{ success, code, message }` error shape.
