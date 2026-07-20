# Bulk Verify US Addresses with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/us_verifications`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Bulk Verify US Addresses](https://docs.lob.com/#tag/US-Verifications/operation/bulk_us_verifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses[]` | body | `array<object>` | yes | An array of up to 20 US verification objects. |
| `addresses[].primary_line` | body | `string` | yes | The primary delivery line for each address. |
| `addresses[].city` | body | `string` | no | The city for each address. Required when ZIP Code is not provided. |
| `addresses[].state` | body | `string` | no | The state for each address. Required when ZIP Code is not provided. |
| `addresses[].zip_code` | body | `string` | no | The ZIP code for each address. Can be used instead of City and State. |
