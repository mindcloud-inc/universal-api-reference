# Get Total Users Metric with Countly

Retrieves the total users metric from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Total Users Metric](https://api.count.ly/reference/omethodtotal_users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query analytics for. |
| `metric` | query | `string` | no | Countly user metric name to fetch. |
