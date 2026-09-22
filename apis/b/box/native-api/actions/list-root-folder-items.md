# List Root Folder Items with Box

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folder_id/items`
- **Base URL:** `https://api.box.com/2.0`
- **Official documentation:** [List Root Folder Items](https://developer.box.com/reference/get-folders-id-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `string` | yes | Root folder ID. This action is preconfigured to use `0`. |
| `limit` | query | `number` | no | Maximum number of root items to return. |
| `offset` | query | `number` | no | Offset-based pagination start position for root items. |
| `usemarker` | query | `boolean` | no | Set true to use marker-based pagination for root items. |
| `marker` | query | `string` | no | Marker token for the next page of root items. |
| `sort` | query | `string` | no | Optional secondary sort field for root items. |
| `direction` | query | `string` | no | Sort direction: ASC or DESC. |
