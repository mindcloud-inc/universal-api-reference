# Get Business with TaxBandits

Retrieves a business from TaxBandits.

## Endpoint

- **Method:** `GET`
- **Path:** `Business/Get`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Get Business](https://developer.taxbandits.com/docs/business/get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessId` | query | `string` | no | TaxBandits business identifier. |
| `PayerRef` | query | `string` | no | Business payer reference. |
| `TIN` | query | `string` | no | Business EIN or SSN. |
