# Verify Address with Byteplant Address Validator

Retrieves address validation results from Byteplant Address Validator.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/verify`
- **Base URL:** `https://api.address-validator.net`
- **Official documentation:** [Verify Address](https://www.byteplant.com/address-validator/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `StreetAddress` | query | `string` | yes | Street, house number, or complete address. |
| `CountryCode` | query | `string` | yes | Two-letter ISO 3166-1 country code. Use XX for international. |
| `City` | query | `string` | no | City or locality. |
| `State` | query | `string` | no | State or province. |
| `PostalCode` | query | `string` | no | ZIP or postal code. |
| `StreetNumber` | query | `string` | no | House number or building number, when separate from the street address. |
| `AdditionalAddressInfo` | query | `string` | no | Building, unit, apartment, floor, or other extra address details. |
| `Geocoding` | query | `boolean` | no | Include latitude and longitude in the response. |
| `Locale` | query | `string` | no | Output language for countries with multiple postal languages. |
| `OutputCharset` | query | `string` | no | Output character set. |
| `Timeout` | query | `number` | no | Request timeout in seconds. |
