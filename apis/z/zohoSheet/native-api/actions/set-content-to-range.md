# Set Content to Range with Zoho Sheet

Updates the content of a range in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Set Content to Range](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Set-content-to-range)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
| `row` | body | `number` | yes | Row index of the cell from which CSV data will start |
| `column` | body | `number` | yes | Column index of the cell from which CSV data will start |
| `ignore_empty` | body | `boolean` | no | If set to true empty value in CSV data will be ignored |
| `data` | body | `string` | yes | CSV data |
