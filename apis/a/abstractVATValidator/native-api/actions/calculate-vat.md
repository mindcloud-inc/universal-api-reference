# Calculate VAT with Abstract VAT Validator

Calculates VAT-compliant pricing for a country in Abstract VAT Validator.

## Endpoint

- **Method:** `GET`
- **Path:** `/calculate`
- **Base URL:** `https://vat.abstractapi.com/v1`
- **Official documentation:** [Calculate VAT](https://abstractapi-vat.mintlify.app/vat-validation/calculate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | query | `number` | yes | The amount to calculate VAT for or from. |
| `country_code` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code for the transaction. |
| `is_vat_incl` | query | `boolean` | no | Set true when the amount already includes VAT and the API should split VAT out. |
| `vat_category` | query | `string` | no | Optional reduced-rate goods category to apply when supported for the country. |
