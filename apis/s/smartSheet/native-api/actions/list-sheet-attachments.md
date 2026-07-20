# List Sheet Attachments with Smartsheet

Retrieves attachments from a Smartsheet sheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId/attachments`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [List Sheet Attachments](https://developers.smartsheet.com/api/smartsheet/openapi/attachments/attachments-listonsheet)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `includeAll` | query | `boolean` | no |
