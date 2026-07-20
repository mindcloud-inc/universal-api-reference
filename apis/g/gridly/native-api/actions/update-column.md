# Update Column with Gridly

Updates an existing column in a Gridly view.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/views/:viewId/columns/:id`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Update Column](https://www.gridly.com/docs/api/#update-a-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view that contains the column. |
| `id` | path | `string` | yes | The unique identifier of the column to update. |
| `name` | body | `string` | no | The updated name for the column. |
| `languageCode` | body | `string` | no | An updated language code for the column. |
| `localizationType` | body | `string` | no | The updated localization role for the column. |
| `numberFormat` | body | `object` | no | Updated number-format settings for the column. |
| `selection` | body | `object` | no | Updated selection options for the column. |
| `reference` | body | `object` | no | Updated reference settings for the column. |
| `formula` | body | `object` | no | Updated formula settings for the column. |
