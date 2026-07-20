# Get WH Certificate with TaxBandits

Retrieves a withholding certificate from TaxBandits.

## Endpoint

- **Method:** `GET`
- **Path:** `WhCertificate/Get`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Get WH Certificate](https://developer.taxbandits.com/docs/whcertificate/get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BusinessId` | query | `string` | no | Business identifier. |
| `PayeeRef` | query | `string` | no | Payee reference. |
