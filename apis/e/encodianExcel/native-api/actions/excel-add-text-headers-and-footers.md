# Excel - Add Text Header or Footer with Encodian - Excel

Adds a text header or footer to an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExcelAddTextHeadersAndFooters`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Add Text Header or Footer](https://support.encodian.com/hc/en-gb/articles/14938826111260)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `headerLeft` | body | `string` | no |
| `headerCentral` | body | `string` | no |
| `headerRight` | body | `string` | no |
| `footerLeft` | body | `string` | no |
| `footerCentral` | body | `string` | no |
| `footerRight` | body | `string` | no |
