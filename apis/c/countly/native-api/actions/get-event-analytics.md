# Get Event Analytics with Countly

Retrieves all event analytics from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Event Analytics](https://api.count.ly/reference/omethodevents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query analytics for. |
| `period` | query | `string` | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
| `event` | query | `string` | no | Optional event key to query. Omit to fetch event totals where supported by Countly. |
| `events` | query | `string` | no | Optional JSON string array of event keys to query together. |
