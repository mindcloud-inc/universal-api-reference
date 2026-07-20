# Delete Business with TaxBandits

Deletes an existing business from TaxBandits.

## Endpoint

- **Method:** `DELETE`
- **Path:** `Business/Delete`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Delete Business](https://developer.taxbandits.com/docs/business/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessId` | query | `string` | no | TaxBandits business identifier. |
| `EINOrSSN` | query | `string` | no | Business EIN or SSN. |
| `isForceDelete` | query | `string` | no | Set true to force deletion where supported. |
