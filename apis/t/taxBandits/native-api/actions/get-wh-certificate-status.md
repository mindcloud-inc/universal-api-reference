# Get WH Certificate Status with TaxBandits

Retrieves withholding certificate status from TaxBandits.

## Endpoint

- **Method:** `GET`
- **Path:** `WhCertificate/Status`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Get WH Certificate Status](https://developer.taxbandits.com/docs/whcertificate/status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessId` | query | `string` | no | Business identifier. |
| `PayeeRef` | query | `string` | no | Payee reference. |
