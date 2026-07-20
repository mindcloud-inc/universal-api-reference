# Verify Filing Credentials with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves filing credential verification results from the EDGAR API.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.edgarfiling.sec.gov/fm/[:cik]/verify`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Verify Filing Credentials](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | 10-digit EDGAR account CIK. |
