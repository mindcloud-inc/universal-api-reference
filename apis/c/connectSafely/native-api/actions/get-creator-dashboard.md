# Get creator dashboard overview with ConnectSafely

Returns the connected account's own creator dashboard (linkedin.com/dashboard/): the "Track performance" cards — post impressions, total followers, profile viewers and search appearances, each with its period label, period-over-period change and trend direction — plus the "Weekly progress" post and comment counts. Read live from the dashboard SDUI screen on every call (select which connected account with `accountId`); it cannot return another member's dashboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/creator/dashboard`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get creator dashboard overview](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-creator-dashboard-get-creator-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If omitted, uses the default account. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used |
| `postImpressions` | `object` | One "Track performance" card. Values are null when LinkedIn rendered no number. |
| `postImpressions.value` | `number` | The headline number |
| `postImpressions.label` | `string` | Label as shown, including the period, e.g. "Post impressions in 7 days" |
| `postImpressions.changePercent` | `number` | Period-over-period change, e.g. 9 for "9%" |
| `postImpressions.changeDirection` | `list` | Direction of that change |
| `postImpressions.comparison` | `string` | What the change compares against, e.g. "vs. prior 7 days" |
| `totalFollowers` | `object` | One "Track performance" card. Values are null when LinkedIn rendered no number. |
| `totalFollowers.value` | `number` | The headline number |
| `totalFollowers.label` | `string` | Label as shown, including the period, e.g. "Post impressions in 7 days" |
| `totalFollowers.changePercent` | `number` | Period-over-period change, e.g. 9 for "9%" |
| `totalFollowers.changeDirection` | `list` | Direction of that change |
| `totalFollowers.comparison` | `string` | What the change compares against, e.g. "vs. prior 7 days" |
| `profileViewers` | `object` | One "Track performance" card. Values are null when LinkedIn rendered no number. |
| `profileViewers.value` | `number` | The headline number |
| `profileViewers.label` | `string` | Label as shown, including the period, e.g. "Post impressions in 7 days" |
| `profileViewers.changePercent` | `number` | Period-over-period change, e.g. 9 for "9%" |
| `profileViewers.changeDirection` | `list` | Direction of that change |
| `profileViewers.comparison` | `string` | What the change compares against, e.g. "vs. prior 7 days" |
| `searchAppearances` | `object` | One "Track performance" card. Values are null when LinkedIn rendered no number. |
| `searchAppearances.value` | `number` | The headline number |
| `searchAppearances.label` | `string` | Label as shown, including the period, e.g. "Post impressions in 7 days" |
| `searchAppearances.changePercent` | `number` | Period-over-period change, e.g. 9 for "9%" |
| `searchAppearances.changeDirection` | `list` | Direction of that change |
| `searchAppearances.comparison` | `string` | What the change compares against, e.g. "vs. prior 7 days" |
| `weeklyProgress` | `object` |  |
| `weeklyProgress.range` | `string` | Week the counts cover, e.g. "Aug 18–Aug 24" |
| `weeklyProgress.posts` | `number` | Posts published this week |
| `weeklyProgress.comments` | `number` | Comments made this week |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "postImpressions": {
    "value": 4124,
    "label": "Post impressions in 7 days",
    "changePercent": 9,
    "changeDirection": "up",
    "comparison": "vs. prior 7 days"
  },
  "totalFollowers": {
    "value": 461,
    "label": "Total followers",
    "changePercent": 0,
    "changeDirection": "flat",
    "comparison": "vs. prior 7 days"
  },
  "profileViewers": {
    "value": 192,
    "label": "Profile viewers in 90 days",
    "changePercent": 47,
    "changeDirection": "down",
    "comparison": "vs. prior 7 days"
  },
  "searchAppearances": {
    "value": 8,
    "label": "Search appearances Aug 11\u201317",
    "changePercent": 0,
    "changeDirection": "flat",
    "comparison": "vs. Aug 4\u201310"
  },
  "weeklyProgress": {
    "range": "Aug 18\u2013Aug 24",
    "posts": 6,
    "comments": 102
  }
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
