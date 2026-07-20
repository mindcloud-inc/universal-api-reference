# Get Large Segmentation Metadata with Countly

Retrieves large segmentation metadata from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Large Segmentation Metadata](https://api.count.ly/reference/omethodsegmentation_big_meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query large segmentation metadata for. |
| `event` | query | `string` | yes | Event key to query large segmentation metadata for. |
| `prop` | query | `string` | no | Property for large segmentation metadata, such as up.src or up.lv. |
| `search` | query | `string` | no | Regex search in segment values. |
