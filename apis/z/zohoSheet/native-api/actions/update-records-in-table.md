# Update Records in Table with Zoho Sheet

Updates records in a table in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Update Records in Table](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Update-records-in-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `table_name` | body | `string` | yes | Name of the table whose records needs to be updated |
| `table_id` | body | `string` | no | Alternatively table_id can be used instead of table_name |
| `criteria_json` | body | `string` | no | Optional parameter. Can be used to filter records. Provide this value as a valid JSON string. |
| `criteria_pattern` | body | `string` | no | Required when more than 1 criteria is available under criteria_json |
| `first_match_only` | body | `boolean` | no | Optional parameter. If true and if there are multiple records on the specified criteria, records will be updated for first match alone. Otherwise, all the matched records will be updated. |
| `is_case_sensitive` | body | `boolean` | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |
| `data` | body | `string` | yes | The JSON data that needs to be updated. Example:{"Month":"May","Amount":50} Provide this value as a valid JSON string. |
