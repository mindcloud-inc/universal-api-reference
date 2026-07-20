# Excel - Unlock with Encodian - Excel

Unlocks an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/UnlockExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Unlock](https://support.encodian.com/hc/en-gb/articles/14358530634140)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `secureOnOpenPassword` | body | `string` | no |
| `workbookProtectionPassword` | body | `string` | no |
| `worksheetProtectionPassword` | body | `string` | no |
