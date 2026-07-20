# Validate Phone Number by IP with BigDataCloud

Validates a phone number by IP address in BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/phone-number-validate-by-ip`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Validate Phone Number by IP](https://www.bigdatacloud.com/phone-email-verification/phone-number-validation-by-ip-address-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | no | Phone number to validate. |
| `ip` | query | `string` | no | IPv4 or IPv6 address. If omitted, the caller IP address is assumed. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
