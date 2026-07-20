# Compare Excel Spreadsheets (Formulas, Uploads) with Diffchecker

Compares Excel spreadsheets in Diffchecker using formulas from uploads.

## Endpoint

- **Method:** `POST`
- **Path:** `/excel`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Excel Spreadsheets (Formulas, Uploads)](https://www.diffchecker.com/docs/excel/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left_spreadsheet` | body | `file` | yes | Left spreadsheet upload. |
| `right_spreadsheet` | body | `file` | yes | Right spreadsheet upload. |
