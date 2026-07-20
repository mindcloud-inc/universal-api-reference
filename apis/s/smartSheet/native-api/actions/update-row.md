# Update Row with Smartsheet

Updates a row in a Smartsheet sheet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sheets/:sheetId/rows`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Update Row](https://developers.smartsheet.com/api/smartsheet/openapi/rows/update-rows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sheetId` | path | `number` | yes |
| `id` | body | `number` | yes |
| `cells[]` | body | `array<object>` | no |
| `parentId` | body | `number` | no |
| `siblingId` | body | `number` | no |
| `above` | body | `boolean` | no |
| `allowPartialSuccess` | query | `boolean` | no |
| `overrideValidation` | query | `boolean` | no |
