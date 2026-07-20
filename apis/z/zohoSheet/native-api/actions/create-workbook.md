# Create Workbook with Zoho Sheet

Creates a new workbook in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/create`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Create Workbook](https://www.zoho.com/sheet/help/api/v2/#WORKBOOK-Create-workbook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workbook_name` | body | `string` | yes | Name of the new workbook |
| `parent_id` | body | `string` | no | Optional parameter. The unique ID of the destination folder. By default My Folder of Zoho Workdrive is the destination folder. |
