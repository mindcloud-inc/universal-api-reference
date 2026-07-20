# Create column with YouGile

Creates a new column in YouGile.

## Endpoint

- **Method:** `POST`
- **Path:** `/columns`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Create column](https://ru.yougile.com/api-v2#/operations/ColumnController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The column title. |
| `boardId` | body | `string` | yes | The board that owns the column. |
| `color` | body | `number` | no | The numeric color code for the column. |
