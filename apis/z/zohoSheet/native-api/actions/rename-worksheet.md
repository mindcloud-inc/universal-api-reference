# Rename Worksheet with Zoho Sheet

Renames an existing worksheet in Zoho Sheet.

## Endpoint

- **Method:** `POST`
- **Path:** `/:resourceId`
- **Base URL:** `https://sheet.zoho.com/api/v2/`
- **Official documentation:** [Rename Worksheet](https://www.zoho.com/sheet/help/api/v2/#WORKSHEET-Rename-worksheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The workbook resource ID. |
| `old_name` | body | `string` | yes | Name of the existing worksheet |
| `new_name` | body | `string` | yes | New name that needs to be set |
