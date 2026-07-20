# Generate CCC with United States Securities and Exchange Commission (SEC) EDGAR Database

Updates a filer's CCC with a generated value in EDGAR.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.edgarfiling.sec.gov/fm/[:cik]/ccc`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Generate CCC](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | 10-digit EDGAR account CIK. |
