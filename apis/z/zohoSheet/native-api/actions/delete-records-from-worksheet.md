# Delete Records from Worksheet with Zoho Sheet

Deletes records from a worksheet in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Delete Records from Worksheet](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Delete-records-from-worksheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet whose records needs to be deleted |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `header_row` | body | `number` | no | Optional parameter. By default, first row of the worksheet is considered as header row. This can be used if tabular data starts from any row other than the first row. |
| `criteria` | body | `string` | no | Mention the criteria as described above. |
| `row_array` | body | `string` | no | Array of row indexes that need to be deleted. Provide this value as a valid JSON array string such as [4]. |
| `first_match_only` | body | `boolean` | no | Optional parameter. If true and if there are multiple records on the specified criteria, records will be deleted for first match alone. Otherwise, all the matched records will be deleted. This parameter will be ignored if criteria is not mentioned. |
| `is_case_sensitive` | body | `boolean` | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |
| `delete_rows` | body | `boolean` | no | Optional parameter and by default it is false. If true it will delete the rows completely, otherwise the records are only erased by default. |
