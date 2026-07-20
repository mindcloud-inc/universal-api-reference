# Excel - Populate with Encodian - Excel

Populates an Excel workbook with JSON data in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/PopulateExcel`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Populate](https://support.encodian.com/hc/en-gb/articles/12736409527324)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | — |
| `jsonData` | body | `string` | yes | — |
| `jsonParseMode` | body | `list<string>` | no | Accepted values: `Standard`, `Strict`. |
