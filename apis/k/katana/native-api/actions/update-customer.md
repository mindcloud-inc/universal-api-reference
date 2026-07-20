# Update Customer with Katana

Updates an existing customer in Katana.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Customer](https://developer.katanamrp.com/reference/updatecustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer id |
| `name` | body | `string` | yes | — |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `currency` | body | `string` | no | The customer’s currency (ISO 4217). |
| `reference_id` | body | `string` | no | Maximum length: 100. |
| `category` | body | `string` | no | Maximum length: 100. |
| `comment` | body | `string` | no | — |
| `discount_rate` | body | `number` | no | — |
| `default_shipping_id` | body | `number` | no | — |
