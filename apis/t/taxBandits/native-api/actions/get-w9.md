# Get W-9 with TaxBandits

Retrieves a W-9 from TaxBandits.

## Endpoint

- **Method:** `GET`
- **Path:** `FormW9/Get`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Get W-9](https://developer.taxbandits.com/docs/formw9/get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessId` | query | `string` | no | Business identifier. |
| `Email` | query | `string` | no | Payee email. |
| `PayeeRef` | query | `string` | no | Payee reference. |
| `TIN` | query | `string` | no | Business EIN or SSN. |
