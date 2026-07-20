# Create Custom CCC with United States Securities and Exchange Commission (SEC) EDGAR Database

Updates a filer's CCC to a custom value in EDGAR.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://api.edgarfiling.sec.gov/fm/[:cik]/ccc`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Create Custom CCC](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | 10-digit EDGAR account CIK. |
| `ccc` | body | `string` | yes | Current EDGAR CCC for the filer. |
| `newCCC` | body | `string` | yes | New custom EDGAR CCC to set for the filer. |
