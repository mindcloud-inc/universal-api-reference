# Fetch Records from Table with Zoho Sheet

Retrieves records from a table in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Fetch Records from Table](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Fetch-records-from-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `table_name` | body | `string` | yes | Name of the table whose records needs to be fetched |
| `table_id` | body | `string` | no | Alternatively table_id can be used instead of table_name |
| `criteria_json` | body | `string` | no | Optional parameter. Can be used to filter records. Provide this value as a valid JSON string. |
| `criteria_pattern` | body | `string` | no | Required when more than 1 criteria is available under criteria_json |
| `column_names` | body | `string` | no | Optional parameter. Can be used to read particular columns data. By default all the columns data will be available in response. Multiple column names must be separated by comma. |
| `render_option` | body | `string` | no | Optional parameter. It defines how the value should be rendered. Possible options are formatted, unformatted, and formula. |
| `count` | body | `number` | no | Optional parameter. It denotes the number of records. |
| `is_case_sensitive` | body | `boolean` | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |
