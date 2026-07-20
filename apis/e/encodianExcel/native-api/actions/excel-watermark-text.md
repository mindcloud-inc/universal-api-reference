# Excel - Add Text Watermark with Encodian - Excel

Adds a text watermark to an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExcelWatermarkText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Add Text Watermark](https://support.encodian.com/hc/en-gb/articles/14428316059420)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileContent` | body | `file` | yes |
| `text` | body | `string` | yes |
| `rowPosition` | body | `number` | yes |
| `columnPosition` | body | `number` | yes |
| `height` | body | `number` | yes |
| `width` | body | `number` | yes |
