# Get Screenshots From Configuration with PagePixels

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot_configs/:screenshot_config_id/screenshots`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [Get Screenshots From Configuration](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `screenshot_config_id` | path | `string` | yes | The screenshot configuration ID whose screenshots should be listed. |
| `page` | query | `number` | no | The result page to retrieve. |
| `limit` | query | `number` | no | The number of records to retrieve. |
| `after` | query | `number` | no | Only include records created after this unix timestamp. |
| `before` | query | `number` | no | Only include records created before this unix timestamp. |
| `order` | query | `string` | no | Sort order, either ASC or DESC. |
