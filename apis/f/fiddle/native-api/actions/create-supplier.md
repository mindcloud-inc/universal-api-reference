# Create Supplier with Fiddle

Creates a new supplier in Fiddle.

## Endpoint

- **Method:** `POST`
- **Path:** `/suppliers`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [Create Supplier](https://fiddle.io/rest/api/v2/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Supplier name |
| `email` | body | `string` | no | Supplier email |
| `phone` | body | `string` | no | Supplier phone |
| `address` | body | `string` | no | Supplier address line 1 |
| `address2` | body | `string` | no | Supplier address line 2 |
| `city` | body | `string` | no | Supplier city |
| `state` | body | `string` | no | Supplier state |
| `zip` | body | `string` | no | Supplier ZIP or postal code |
| `country` | body | `string` | no | Supplier country |
| `fax` | body | `string` | no | Supplier fax |
| `billingAddressInput` | body | `object` | no | Billing address object |
| `shippingAddressInput` | body | `object` | no | Shipping address object |
| `contacts[]` | body | `array<object>` | no | Array of supplier contacts |
