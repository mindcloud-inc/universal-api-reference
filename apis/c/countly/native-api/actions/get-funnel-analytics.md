# Get Funnel Analytics with Countly

Retrieves all funnel analytics from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Funnel Analytics](https://api.count.ly/reference/omethodfunnel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query funnel analytics for. |
| `funnel` | query | `string` | yes | Countly funnel ID to fetch analytics for. |
| `period` | query | `string` | no | Countly reporting period for funnel data. |
