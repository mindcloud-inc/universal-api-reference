# Create Column with Gridly

Creates a new column in a Gridly view.

## Endpoint

- **Method:** `POST`
- **Path:** `/views/:viewId/columns`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Create Column](https://www.gridly.com/docs/api/#create-a-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view where the column should be created. |
| `name` | body | `string` | yes | The display name of the column to create. |
| `type` | body | `string` | yes | The Gridly column type to create. |
| `id` | body | `string` | no | An optional explicit column ID to assign when creating the column. |
| `languageCode` | body | `string` | no | A language code for language columns. |
| `localizationType` | body | `string` | no | The localization role for language columns, such as sourceLanguage or targetLanguage. |
| `numberFormat` | body | `object` | no | Number-format settings for number columns. |
| `selection` | body | `object` | no | Selection options for singleSelection or multipleSelections columns. |
| `reference` | body | `object` | no | Reference settings for reference columns. |
| `formula` | body | `object` | no | Formula settings for formula columns. |
