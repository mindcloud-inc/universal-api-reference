# Create Table with Zoho Sheet

Creates a new table in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Create Table](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Create-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `start_row` | body | `number` | yes | start row index of the table |
| `start_column` | body | `number` | yes | start column index of the table |
| `end_row` | body | `number` | yes | end row index of the table |
| `end_column` | body | `number` | yes | end column index of the table |
| `contains_header` | body | `boolean` | no | Optional parameter. The default value is true. If set to false, the header row will be inserted at the top as an additional row to the selected range. |
| `header_names` | body | `string` | no | Optional parameter. Array of header values for the created table. The header_names must be unique. For example : ["country","region"]. The length of header_names and column length of the table must be equal. Provide this value as a valid JSON string. |
| `table_style` | body | `string` | no | Optional parameter. A json array of styles and properties for table. The template and color values correspond to the options provided in the spreadsheet. Instead of the predefined color options (Accent1 to Accent6), hex color codes can also be used. Example: {"template":"light1", "color":"#FF5733", "properties" : {"first_column":true, "last_column":true, "banded_rows":true, "banded_columns":false, "total_row":false}}. The default table_styles for a table is {"template":"Medium1", "color":"Accent1", "properties": {"first_column":false, "last_column":false, "banded_rows":true, "banded_columns":false, "total_row":false}} Provide this value as a valid JSON string. |
