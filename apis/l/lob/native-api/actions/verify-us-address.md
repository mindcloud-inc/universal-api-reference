# Verify US Address with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/us_verifications`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Verify US Address](https://docs.lob.com/#tag/US-Verifications/operation/us_verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primary_line` | body | `string` | yes | The primary delivery line to verify. |
| `city` | body | `string` | no | The city. Required when ZIP Code is not provided. |
| `state` | body | `string` | no | The ISO 3166-2 two-letter state code or subdivision name. Required when ZIP Code is not provided. |
| `zip_code` | body | `string` | no | The ZIP code. Can be used instead of City and State. |
