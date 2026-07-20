# Validate State or Province with Cloudmersive

Validates a state or province in Cloudmersive.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/address/state`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Validate State or Province](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-state-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CountryCode` | body | `string` | no | Optional two-letter country code. |
| `CountryFullName` | body | `string` | no | Optional country name. |
| `StateOrProvince` | body | `string` | no | State or province to validate. |
