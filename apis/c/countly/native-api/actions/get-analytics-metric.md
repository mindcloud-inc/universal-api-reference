# Get Analytics Metric with Countly

Retrieves an analytics metric from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/analytics/metric`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Analytics Metric](https://api.count.ly/reference/oanalyticsmetric)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query analytics for. |
| `metric` | query | `string` | yes | Metric name available from Countly /o?method APIs. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
