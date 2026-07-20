# Validate Phone Number with BigDataCloud

Validates a phone number in BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/phone-number-validate`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Validate Phone Number](https://www.bigdatacloud.com/phone-email-verification/phone-number-validation-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | no | Phone number to validate. |
| `countryCode` | query | `string` | no | Country code in ISO 3166-1 Alpha-2, Alpha-3, or numeric format. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
