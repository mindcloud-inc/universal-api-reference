# Excel - Remove Text Watermark with Encodian - Excel

Removes text watermarks from an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExcelWatermarkTextRemove`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Remove Text Watermark](https://support.encodian.com/hc/en-gb/articles/14449860203548)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `watermarkId` | body | `number` | yes |
