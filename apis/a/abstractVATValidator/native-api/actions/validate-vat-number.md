# Validate VAT Number with Abstract VAT Validator

Validates a VAT number and returns company details from Abstract VAT Validator.

## Endpoint

- **Method:** `GET`
- **Path:** `/validate`
- **Base URL:** `https://vat.abstractapi.com/v1`
- **Official documentation:** [Validate VAT Number](https://abstractapi-vat.mintlify.app/vat-validation/validate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vat_number` | query | `string` | yes | The VAT number to validate. |
