# List VAT Rates with VAT Comply

Retrieves VAT rates from VAT Comply.

## Endpoint

- **Method:** `GET`
- **Path:** `/vat_rates`
- **Base URL:** `https://api.vatcomply.com`
- **Official documentation:** [List VAT Rates](https://www.vatcomply.com/api/vat-rates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Filter by EU member state code, for example DE or FR. |
