# List W-9s with TaxBandits

Retrieves W-9 records from TaxBandits.

## Endpoint

- **Method:** `GET`
- **Path:** `FormW9/List`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [List W-9s](https://developer.taxbandits.com/docs/formw9/list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessId` | query | `string` | no | Business identifier. |
| `Page` | query | `string` | no | Page number. |
| `PageSize` | query | `string` | no | Records per page. |
| `TIN` | query | `string` | no | Business EIN or SSN. |
| `W9Status` | query | `string` | no | Filter by W-9 status. |
