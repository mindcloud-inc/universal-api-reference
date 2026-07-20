# Get Individuals with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves filer-associated individuals from the EDGAR API.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.edgarfiling.sec.gov/fm/[:cik]/individuals`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Individuals](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | 10-digit EDGAR account CIK. |
