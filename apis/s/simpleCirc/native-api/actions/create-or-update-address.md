# Create or Update Address with SimpleCirc

Creates or updates a subscriber address in SimpleCirc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.2/subscribers/:account_id/addresses`
- **Base URL:** `https://simplecirc.com`
- **Official documentation:** [Create or Update Address](https://simplecirc.com/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `address_1` | body | `string` | yes |
| `address_2` | body | `string` | no |
| `city` | body | `string` | yes |
| `state` | body | `string` | yes |
| `zipcode` | body | `string` | yes |
| `country` | body | `string` | no |
