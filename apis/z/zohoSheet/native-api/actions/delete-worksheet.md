# Delete Worksheet with Zoho Sheet

Deletes an existing worksheet from Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Delete Worksheet](https://www.zoho.com/sheet/help/api/v2/#WORKSHEET-Delete-worksheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `worksheet_name` | body | `string` | yes | Name of the worksheet that needs to be deleted |
| `worksheet_id` | body | `string` | no | Alternatively worksheet_id can be used instead of worksheet_name |
