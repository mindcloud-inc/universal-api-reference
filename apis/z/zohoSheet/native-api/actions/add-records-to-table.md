# Add Records to Table with Zoho Sheet

Adds records to a table in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Add Records to Table](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Add-records-to-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `table_name` | body | `string` | yes | Name of the table |
| `table_id` | body | `string` | no | Alternatively table_id can be used instead of table_name |
| `insert_at_top` | body | `boolean` | no | Optional parameter. Can be set as true to add records at the top. By default it is false. |
| `json_data` | body | `string` | yes | JSON Array. Example : [{"Name":"Joe","Region":"South","Units":284},{"Name":"Beth","Region":"East","Units":290}]. "Name", "Region", and "Units" are the table headers. Provide this value as a valid JSON string. |
