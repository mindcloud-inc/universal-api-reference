# Validate VAT Number with VatcheckAPI

Validates a VAT number in VatcheckAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/check`
- **Base URL:** `https://api.vatcheckapi.com`
- **Official documentation:** [Validate VAT Number](https://vatcheckapi.com/docs/check.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vat_number` | query | `string` | yes | VAT number to query. It can include the country prefix, or be provided with Country Code. |
| `country_code` | query | `string` | no | ISO Alpha-2 country code for the VAT number, for example LU. Required only when the VAT number does not include its country prefix. Maximum length: 2. |
