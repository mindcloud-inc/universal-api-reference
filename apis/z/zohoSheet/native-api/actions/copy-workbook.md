# Copy Workbook with Zoho Sheet

Creates a copy of a workbook in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/copy`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Copy Workbook](https://www.zoho.com/sheet/help/api/v2/#WORKBOOK-Copy-workbook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_id` | body | `string` | yes | The resource id of the workbook that needs to be copied |
| `workbook_name` | body | `string` | no | Optional parameter. Name of the copied workbook |
| `parent_id` | body | `string` | no | Optional parameter. The unique ID of the destination folder. By default My Folder of Zoho Workdrive is the destination folder. |
| `copy_lock_settings` | body | `boolean` | no | Optional parameter. Default value is true. If set to false the range/worksheet lock settings from the parent document will not be copied. |
