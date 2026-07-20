# Get Content of Range with Zoho Sheet

Retrieves the content of a range in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Get Content of Range](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Get-content-of-range)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `start_row` | body | `number` | yes | Start row index of the range |
| `start_column` | body | `number` | yes | Start column index of the range |
| `end_row` | body | `number` | yes | End row index of the range |
| `end_column` | body | `number` | yes | End column index of the range |
