# List Change Notifications with PagePixels

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot_configs/:screenshot_config_id/change_notifications`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [List Change Notifications](https://pagepixels.com/app/screenshots-api-documentation#show-all-changes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `screenshot_config_id` | path | `string` | yes | The screenshot configuration ID to inspect for change notifications. |
| `page` | query | `number` | no | The page to retrieve. |
| `limit` | query | `number` | no | The maximum number of notifications to return. |
| `after` | query | `number` | no | Only return notifications created after this unix timestamp. |
| `before` | query | `number` | no | Only return notifications created before this unix timestamp. |
| `order` | query | `string` | no | Sort order: ASC or DESC. |
