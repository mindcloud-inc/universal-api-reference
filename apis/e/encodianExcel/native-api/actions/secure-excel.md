# Excel - Secure with Encodian - Excel

Secures and protects an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/SecureExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Secure](https://support.encodian.com/hc/en-gb/articles/14332917020188)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | — |
| `secureOnOpenPassword` | body | `string` | no | — |
| `workbookProtectionType` | body | `list<string>` | no | Accepted values: `All`, `None`, `Structure`, `Windows`. |
| `workbookProtectionPassword` | body | `string` | no | — |
| `worksheetProtectionType` | body | `list<string>` | no | Accepted values: `All`, `Contents`, `None`, `Objects`, `Scenarios`. |
| `worksheetProtectionPassword` | body | `string` | no | — |
