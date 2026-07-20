# Fetch Records from Worksheet with Zoho Sheet

Retrieves records from a worksheet in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Fetch Records from Worksheet](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Fetch-records-from-worksheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet whose records needs to be fetched |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `header_row` | body | `number` | no | Optional parameter. By default, first row of the worksheet is considered as header row. This can be used if tabular data starts from any row other than the first row. |
| `criteria` | body | `string` | no | Optional parameter. Can be used to filter records. |
| `column_names` | body | `string` | no | Optional parameter. Can be used to read particular column's data. By default all the column data will be available in response. Multiple column names must be separated by comma. |
| `render_option` | body | `string` | no | Optional parameter. It defines how the value should be rendered. Possible options are formatted, unformatted, and formula. |
| `records_start_index` | body | `number` | no | Optional parameter. This parameter can be used to get a few resources if there are too many. |
| `count` | body | `number` | no | Optional parameter. It denotes the number of records. |
| `is_case_sensitive` | body | `boolean` | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |
