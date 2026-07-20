# Validate Order Address with Snappy

Validates a shipping address in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/addresses/validate`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Validate Order Address](https://docs.snappy.com/reference/validateorderaddress)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `object` | yes |
| `companyId` | query | `string` | yes |
| `country` | body | `string` | yes |
