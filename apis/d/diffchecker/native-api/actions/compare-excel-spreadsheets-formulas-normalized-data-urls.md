# Compare Excel Spreadsheets (Formulas, Normalized, Data URLs) with Diffchecker

Compares Excel spreadsheets in Diffchecker using normalized formulas from data URLs.

## Endpoint

- **Method:** `POST`
- **Path:** `/excel`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Excel Spreadsheets (Formulas, Normalized, Data URLs)](https://www.diffchecker.com/docs/excel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left_spreadsheet` | body | `string` | yes | Left spreadsheet as a data URL. |
| `right_spreadsheet` | body | `string` | yes | Right spreadsheet as a data URL. |
