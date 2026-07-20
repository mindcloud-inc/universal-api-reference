# Get Campaign Data with Countly

Retrieves all campaign data from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/campaign`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Campaign Data](https://api.count.ly/reference/ocampaigndata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query campaign data for. |
| `data` | query | `string` | yes | JSON string array of campaign IDs to fetch action data for. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
