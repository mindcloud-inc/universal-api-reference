# Get Filer Account Information with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves filer account information from the EDGAR API.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.edgarfiling.sec.gov/fm/[:cik]`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Filer Account Information](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | 10-digit EDGAR account CIK. |
