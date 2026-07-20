# Get VAT Categories with Abstract VAT Validator

Retrieves VAT rate categories for a country from Abstract VAT Validator.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories`
- **Base URL:** `https://vat.abstractapi.com/v1`
- **Official documentation:** [Get VAT Categories](https://abstractapi-vat.mintlify.app/vat-validation/categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code to retrieve VAT categories for. |
