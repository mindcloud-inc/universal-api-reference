# Export saved transactions with ID Analyzer

Creates a saved transaction export in ID Analyzer.

## Endpoint

- **Method:** `POST`
- **Path:** `/export/transaction`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Export saved transactions](https://developer.idanalyzer.com/reference/post-export-transaction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exportType` | body | `string` | yes | Export format: csv or json. |
