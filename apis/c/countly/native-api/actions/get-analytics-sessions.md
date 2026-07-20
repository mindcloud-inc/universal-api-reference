# Get Analytics Sessions with Countly

Retrieves all analytics sessions from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/analytics/sessions`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Analytics Sessions](https://api.count.ly/reference/oanalyticssessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query analytics for. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
