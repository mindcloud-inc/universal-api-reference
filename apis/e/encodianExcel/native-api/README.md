# Encodian - Excel: Native API Reference

A consolidated summary of Encodian - Excel's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-gb/connectors/encodianexcel/
- **OpenAPI specification:** https://api.apps-encodian.com/swagger/Excel/swagger.json
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Use an Encodian Flowr API key. Encodian documents the API key as required for the Excel connector, sent to the API with the X-ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://support.encodian.com/hc/en-gb/articles/360012267353-Create-an-Encodian-Connection-in-Power-Automate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Excel - Add Rows](actions/add-rows-to-excel.md) | `POST /api/v1/Excel/AddRowsToExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/11551842583581) |
| [CSV - Parse](actions/csv-parse.md) | `POST /api/v1/Excel/ParseCsv` | [docs](https://support.encodian.com/hc/en-gb/articles/360005177297-Parse-CSV) |
| [Excel - Delete Worksheets](actions/delete-excel-worksheets.md) | `POST /api/v1/Excel/DeleteExcelWorksheets` | [docs](https://support.encodian.com/hc/en-gb/articles/13233342312220) |
| [Excel - Delete Rows](actions/delete-rows-from-excel.md) | `POST /api/v1/Excel/DeleteRowsFromExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/9936160309148) |
| [Excel - Add Image Header or Footer](actions/excel-add-image-header-or-footer.md) | `POST /api/v1/Excel/ExcelAddImageHeaderOrFooter` | [docs](https://support.encodian.com/hc/en-gb/articles/14909213525404) |
| [Excel - Add Text Header or Footer](actions/excel-add-text-headers-and-footers.md) | `POST /api/v1/Excel/ExcelAddTextHeadersAndFooters` | [docs](https://support.encodian.com/hc/en-gb/articles/14938826111260) |
| [Excel - Remove Headers and Footers](actions/excel-remove-headers-and-footers.md) | `POST /api/v1/Excel/ExcelRemoveHeadersAndFooters` | [docs](https://support.encodian.com/hc/en-gb/articles/14943764511900) |
| [Excel - Replace Text](actions/excel-replace-text.md) | `POST /api/v1/Excel/ExcelReplaceText` | [docs](https://support.encodian.com/hc/en-gb/articles/16811169514652) |
| [Excel - Separate Worksheets](actions/excel-separate-worksheets.md) | `POST /api/v1/Excel/ExcelSeparateWorksheets` | [docs](https://support.encodian.com/hc/en-gb/articles/21049256666908) |
| [Excel - Add Text Watermark](actions/excel-watermark-text.md) | `POST /api/v1/Excel/ExcelWatermarkText` | [docs](https://support.encodian.com/hc/en-gb/articles/14428316059420) |
| [Excel - Remove Text Watermark](actions/excel-watermark-text-remove.md) | `POST /api/v1/Excel/ExcelWatermarkTextRemove` | [docs](https://support.encodian.com/hc/en-gb/articles/14449860203548) |
| [Excel - Extract Worksheets](actions/extract-excel-worksheets.md) | `POST /api/v1/Excel/ExtractExcelWorksheets` | [docs](https://support.encodian.com/hc/en-gb/articles/13230802892316) |
| [Excel - Extract Rows](actions/get-rows-from-excel.md) | `POST /api/v1/Excel/GetRowsFromExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/9390845334172) |
| [Excel - Merge Files](actions/merge-array-of-excel-documents.md) | `POST /api/v1/Excel/MergeArrayOfExcelDocuments` | [docs](https://support.encodian.com/hc/en-gb/articles/4469865776529) |
| [Excel - Merge Rows](actions/merge-excel-rows.md) | `POST /api/v1/Excel/MergeExcelRows` | [docs](https://support.encodian.com/hc/en-gb/articles/11345445953820) |
| [Excel - Populate](actions/populate-excel.md) | `POST /api/v1/Excel/PopulateExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/12736409527324) |
| [Excel - Secure](actions/secure-excel.md) | `POST /api/v1/Excel/SecureExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/14332917020188) |
| [Excel - Unlock](actions/unlock-excel.md) | `POST /api/v1/Excel/UnlockExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/14358530634140) |
| [Excel - Update Rows](actions/update-rows-in-excel.md) | `POST /api/v1/Excel/UpdateRowsInExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/11205752671004) |
