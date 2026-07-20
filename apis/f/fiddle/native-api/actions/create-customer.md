# Create Customer with Fiddle

Creates a new customer in Fiddle.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [Create Customer](https://fiddle.io/rest/api/v2/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Customer name |
| `email` | body | `string` | no | Customer email |
| `phone` | body | `string` | no | Customer phone |
| `address` | body | `string` | no | Customer address line 1 |
| `address2` | body | `string` | no | Customer address line 2 |
| `city` | body | `string` | no | Customer city |
| `state` | body | `string` | no | Customer state |
| `zip` | body | `string` | no | Customer ZIP or postal code |
| `country` | body | `string` | no | Customer country |
| `fax` | body | `string` | no | Customer fax |
| `billingAddressInput` | body | `object` | no | Billing address object |
| `shippingAddressInput` | body | `object` | no | Shipping address object |
| `contacts[]` | body | `array<object>` | no | Array of customer contacts |
