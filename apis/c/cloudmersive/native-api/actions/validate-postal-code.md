# Validate Postal Code with Cloudmersive

Validates a postal code in Cloudmersive.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/address/postal-code`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate Postal Code](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-postal-code-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CountryCode` | body | `string` | no | Optional two-letter country code. |
| `CountryFullName` | body | `string` | no | Optional country name. |
| `PostalCode` | body | `string` | no | Postal or ZIP code to validate. |
