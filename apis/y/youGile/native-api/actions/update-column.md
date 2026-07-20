# Update column with YouGile

Updates an existing column in YouGile.

## Endpoint

- **Method:** `PUT`
- **Path:** `/columns/:id`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Update column](https://ru.yougile.com/api-v2#/operations/ColumnController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The YouGile column ID. |
| `title` | body | `string` | no | The updated column title. |
| `boardId` | body | `string` | no | The board that owns the column. |
| `color` | body | `number` | no | The numeric color code for the column. |
| `deleted` | body | `boolean` | no | Mark the column as deleted. |
