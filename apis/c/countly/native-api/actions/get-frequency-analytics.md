# Get Frequency Analytics with Countly

Retrieves all frequency analytics from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/analytics/frequency`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Frequency Analytics](https://api.count.ly/reference/oanalyticsfrequency)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query analytics for. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
