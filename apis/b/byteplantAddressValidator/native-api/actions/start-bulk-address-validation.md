# Start Bulk Address Validation with Byteplant Address Validator

Creates a bulk address validation task in Byteplant Address Validator.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/bulk-verify`
- **Base URL:** `https://api.address-validator.net`
- **Official documentation:** [Start Bulk Address Validation](https://www.byteplant.com/address-validator/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressesCsv` | body | `string` | yes | CSV content with address rows for bulk validation. |
| `CountryCode` | query | `string` | no | Optional two-letter ISO 3166-1 country code. Use XX for international. |
| `Geocoding` | query | `boolean` | no | Include latitude and longitude in bulk validation results. |
| `OutputCharset` | query | `string` | no | Output character set. |
| `Locale` | query | `string` | no | Output language for countries with multiple postal languages. |
| `TaskName` | query | `string` | no | Optional name for the bulk validation task. |
| `NotifyEmail` | query | `string` | no | Optional email address to receive task completion notifications. |
| `NotifyURL` | query | `string` | no | Optional URL to receive task completion notifications. |
