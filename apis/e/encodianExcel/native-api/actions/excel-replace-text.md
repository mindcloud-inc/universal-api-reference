# Excel - Replace Text with Encodian - Excel

Finds and replaces text in an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExcelReplaceText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Replace Text](https://support.encodian.com/hc/en-gb/articles/16811169514652)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | — |
| `phrases[]` | body | `array<object>` | yes | Array of replacement phrase objects with searchText and optional replacementText. |
| `cultureName` | body | `string` | no | — |
