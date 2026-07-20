# Excel - Merge Rows with Encodian - Excel

Merges rows from Excel files into one worksheet in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/MergeExcelRows`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Merge Rows](https://support.encodian.com/hc/en-gb/articles/11345445953820)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | no | Filename of the output Excel file. |
| `outputFormat` | body | `list<string>` | yes | Accepted values: `CSV`, `PDF`, `TIFF`, `XLS`, `XLSB`, `XLSM`, `XLSX`. |
| `documents[]` | body | `array<object>` | yes | Array of source file objects with fileName, fileContent, and optional sortPosition. |
| `preserveFirstRow` | body | `boolean` | no | — |
