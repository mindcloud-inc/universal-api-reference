# Get Segmentation with Countly

Retrieves all segmentation data from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Segmentation](https://api.count.ly/reference/omethodsegmentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query segmentation for. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
| `event` | query | `string` | yes | Event key to query segmentation for. |
| `bucket` | query | `string` | no | Breakdown period for segmentation, such as hourly, daily, weekly, or monthly. |
| `projectionKey` | query | `string` | no | Show top results by a specific segment value. |
| `queryObject` | query | `string` | no | JSON string encoded MongoDB query for segmentation. |
