# Create Customer Address with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/customers/addresses`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `first_name` | body | `string` | yes |
| `last_name` | body | `string` | yes |
| `company` | body | `string` | no |
| `address1` | body | `string` | yes |
| `address2` | body | `string` | no |
| `city` | body | `string` | yes |
| `state_or_province` | body | `string` | yes |
| `postal_code` | body | `string` | yes |
| `country_code` | body | `string` | yes |
| `phone` | body | `string` | no |
| `address_type` | body | `string` | no |
| `customer_id` | body | `string` | yes |
