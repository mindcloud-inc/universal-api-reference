# Register Shipping Address with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/addresses`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Register Shipping Address](https://developer.shipandco.com/en/#shipping-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Recipient company. Required unless full name is provided. |
| `email` | body | `string` | no | Email address. |
| `full_name` | body | `string` | no | Recipient full name. Required unless company is provided. |
| `province` | body | `string` | no | Province or state code/name as required by destination country. |
| `country` | body | `string` | yes | ISO country code. |
| `zip` | body | `string` | yes | Postal code. |
| `address1` | body | `string` | yes | Primary street address. |
| `phone` | body | `string` | yes | Phone number. |
