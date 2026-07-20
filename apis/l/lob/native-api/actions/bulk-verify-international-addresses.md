# Bulk Verify International Addresses with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/intl_verifications`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Bulk Verify International Addresses](https://docs.lob.com/#tag/Intl-Verifications/operation/bulk_intl_verifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses[]` | body | `array<object>` | yes | An array of up to 20 international verification objects. |
| `addresses[].primary_line` | body | `string` | yes | The primary delivery line for each international address. |
| `addresses[].country` | body | `string` | yes | The 2-letter ISO 3166 country code for each address. |
| `addresses[].recipient` | body | `string` | no | The recipient for each address. |
| `addresses[].secondary_line` | body | `string` | no | The secondary delivery line for each address. |
| `addresses[].city` | body | `string` | no | The city for each address. |
| `addresses[].state` | body | `string` | no | The state or province for each address. |
| `addresses[].postal_code` | body | `string` | no | The postal code for each address. |
