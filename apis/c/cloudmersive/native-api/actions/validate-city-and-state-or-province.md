# Validate City and State or Province with Cloudmersive

Validates a city and state or province in Cloudmersive.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/address/city`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate City and State or Province](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-city-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `City` | body | `string` | no | City to validate. |
| `CountryCode` | body | `string` | no | Optional two-letter country code. |
| `CountryFullName` | body | `string` | no | Optional country name. |
| `StateOrProvince` | body | `string` | no | State or province to validate. |
