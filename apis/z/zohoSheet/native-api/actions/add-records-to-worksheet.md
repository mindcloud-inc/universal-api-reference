# Add Records to Worksheet with Zoho Sheet

Adds records to a worksheet in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Add Records to Worksheet](https://www.zoho.com/sheet/help/api/v2/#TABULAR-Add-records-to-worksheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `header_row` | body | `number` | no | Optional parameter. Default value is 1. This can be mentioned if the table header is not in the first row of the worksheet. |
| `json_data` | body | `string` | yes | JSON Array. Example : [{"Name":"Joe","Region":"South","Units":284},{"Name":"Beth","Region":"East","Units":290}]. "Name", "Region", and "Units" are the table headers. Provide this value as a valid JSON string. |
