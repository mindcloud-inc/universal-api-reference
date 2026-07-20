# Excel - Merge Files with Encodian - Excel

Merges Excel files into one file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/MergeArrayOfExcelDocuments`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Merge Files](https://support.encodian.com/hc/en-gb/articles/4469865776529)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | no | Filename of the output Excel file. |
| `mergeExcelOutputFormat` | body | `list<string>` | no | Accepted values: `CSV`, `PDF`, `TIFF`, `XLS`, `XLSB`, `XLSM`, `XLSX`. |
| `documents[]` | body | `array<object>` | yes | Array of source file objects with fileName, fileContent, and optional sortPosition. |
