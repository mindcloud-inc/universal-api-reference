# Update Ad with Curator

Updates an existing ad or custom post in Curator.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.2/ads/:AD_ID`
- **Base URL:** `https://api.curator.io`
- **Official documentation:** [Update Ad](https://curator.io/docs/api/ads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AD_ID` | path | `string` | yes | ID of the ad to update. |
| `feed_id` | body | `string` | yes | Feed to assign the ad to. |
| `network_id` | body | `number` | yes | Network identifier for the ad. |
| `name` | body | `string` | yes | Ad name. |
| `position_start` | body | `number` | yes | Starting position for the ad. |
| `position_repeats` | body | `boolean` | yes | Whether the ad repeats. |
| `position_repeat_interval` | body | `number` | no | Repeat interval when repeating is enabled. |
| `text` | body | `string` | yes | Ad text. |
| `status` | body | `string` | yes | Ad status. |
| `click_action` | body | `string` | yes | Behavior when the ad is clicked. |
| `url` | body | `string` | no | Target URL when click action is goto-url. |
| `image_url` | body | `string` | no | Optional external image URL. |
| `video_url` | body | `string` | no | Optional external video URL. |
