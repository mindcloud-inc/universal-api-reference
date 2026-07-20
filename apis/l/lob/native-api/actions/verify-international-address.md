# Verify International Address with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/intl_verifications`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Verify International Address](https://docs.lob.com/#tag/Intl-Verifications/operation/intl_verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primary_line` | body | `string` | yes | The primary delivery line of the international address. |
| `country` | body | `string` | yes | The 2-letter ISO 3166 country code. |
| `recipient` | body | `string` | no | The intended recipient. |
| `secondary_line` | body | `string` | no | The secondary delivery line. |
| `city` | body | `string` | no | The city name. |
| `state` | body | `string` | no | The state or province name. |
| `postal_code` | body | `string` | no | The postal code. |
