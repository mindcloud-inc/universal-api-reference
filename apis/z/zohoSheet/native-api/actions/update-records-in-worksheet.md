# Update Records in Worksheet with Zoho Sheet

Updates records in a worksheet in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Update Records in Worksheet](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Update-records-in-worksheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet whose records needs to be update |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `header_row` | body | `number` | no | Optional parameter. By default, first row of the worksheet is considered as header row. This can be used if tabular data starts from any row other than the first row. |
| `criteria` | body | `string` | no | Optional parameter. If criteria is not set all available rows will get updated. Mention the criteria as described above. |
| `first_match_only` | body | `boolean` | no | Optional parameter. If true and if there are multiple records on the specified criteria, records will be updated for first match alone. Otherwise, all the matched records will be updated. |
| `is_case_sensitive` | body | `boolean` | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |
| `data` | body | `string` | yes | The JSON data that needs to be updated. Example:{"Month":"May","Amount":50} Provide this value as a valid JSON string. |
