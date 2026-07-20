# Get Delegations with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves delegation relationships for an EDGAR filer account.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.edgarfiling.sec.gov/fm/[:cik]/delegations`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Delegations](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | 10-digit EDGAR account CIK. |
