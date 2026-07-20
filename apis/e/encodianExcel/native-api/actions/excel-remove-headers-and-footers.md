# Excel - Remove Headers and Footers with Encodian - Excel

Removes headers and footers from an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExcelRemoveHeadersAndFooters`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Remove Headers and Footers](https://support.encodian.com/hc/en-gb/articles/14943764511900)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `headerLeft` | body | `boolean` | no |
| `headerCentral` | body | `boolean` | no |
| `headerRight` | body | `boolean` | no |
| `footerLeft` | body | `boolean` | no |
| `footerCentral` | body | `boolean` | no |
| `footerRight` | body | `boolean` | no |
