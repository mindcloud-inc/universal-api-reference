# Validate Street Address with Cloudmersive

Validates a street address in Cloudmersive.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/address/street-address`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate Street Address](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-street-address-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `City` | body | `string` | no | City for the address. |
| `CountryCode` | body | `string` | no | Optional two-letter country code. |
| `CountryFullName` | body | `string` | no | Optional country name. |
| `PostalCode` | body | `string` | no | Optional postal or ZIP code. |
| `StateOrProvince` | body | `string` | no | State or province for the address. |
| `StreetAddress` | body | `string` | no | Street address to validate. |
