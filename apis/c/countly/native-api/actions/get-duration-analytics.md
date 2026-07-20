# Get Duration Analytics with Countly

Retrieves all duration analytics from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/analytics/durations`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Duration Analytics](https://api.count.ly/reference/oanalyticsdurations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query analytics for. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
