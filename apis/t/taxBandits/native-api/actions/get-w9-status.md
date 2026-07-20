# Get W-9 Status with TaxBandits

Retrieves W-9 status from TaxBandits.

## Endpoint

- **Method:** `GET`
- **Path:** `FormW9/Status`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Get W-9 Status](https://developer.taxbandits.com/docs/formw9/status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessId` | query | `string` | no | Business identifier. |
| `Email` | query | `string` | no | Payee email. |
| `PayeeRef` | query | `string` | no | Payee reference. |
| `TIN` | query | `string` | no | Business EIN or SSN. |
