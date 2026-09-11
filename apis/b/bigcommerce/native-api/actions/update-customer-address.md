# Update Customer Address with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/customers/addresses`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `company` | body | `string` | no |
| `address1` | body | `string` | no |
| `address2` | body | `string` | no |
| `city` | body | `string` | no |
| `state_or_province` | body | `string` | no |
| `postal_code` | body | `string` | no |
| `country_code` | body | `string` | no |
| `phone` | body | `string` | no |
| `address_type` | body | `string` | no |
