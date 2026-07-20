# Get Segmentation Metadata with Countly

Retrieves all segmentation metadata from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get Segmentation Metadata](https://api.count.ly/reference/omethodsegmentation_meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to query segmentation metadata for. |
| `event` | query | `string` | yes | Event key to query segmentation metadata for. |
