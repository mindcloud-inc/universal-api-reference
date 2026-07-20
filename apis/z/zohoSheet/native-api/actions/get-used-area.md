# Get Used Area with Zoho Sheet

Retrieves the used area of a worksheet in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Get Used Area](https://www.zoho.com/sheet/help/api/v2/#CONTENT-Get-used-area)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
