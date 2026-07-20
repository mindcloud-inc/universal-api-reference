# Create Link Attachment on Sheet with Smartsheet

Creates a link attachment on a Smartsheet sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/sheets/:sheetId/attachments`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Create Link Attachment on Sheet](https://developers.smartsheet.com/api/smartsheet/openapi/attachments/attachments-attachtosheet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `url` | body | `string` | yes |
| `description` | body | `string` | no |
| `attachmentSubType` | body | `string` | no |
