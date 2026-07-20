# Get Variant with Snappy

Retrieves a variant from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/variants/{variantId}`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Get Variant](https://docs.snappy.com/reference/getvariantbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variantId` | path | `string` | yes | Variant ID. |
| `companyId` | query | `string` | no | Company ID. |
| `country` | query | `string` | no | Country. |
| `fields[]` | query | `array<string>` | no | Additional variant fields to include. |
