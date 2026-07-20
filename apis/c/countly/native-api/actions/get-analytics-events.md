# Get Analytics Events with Countly

Retrieves all analytics events from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/analytics/events`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Analytics Events](https://api.count.ly/reference/oanalyticsevents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query analytics for. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
| `event` | query | `string` | no | Event key to query. |
| `events` | query | `string` | no | JSON string array of event keys to query together. |
