# Create Customer with Katana

Creates a new customer in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Customer](https://developer.katanamrp.com/reference/create-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
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
| `addresses[]` | body | `array<object>` | no | — |
| `addresses[].entity_type` | body | `string` | no | — |
| `addresses[].default` | body | `boolean` | no | — |
| `addresses[].first_name` | body | `string` | no | — |
| `addresses[].last_name` | body | `string` | no | — |
| `addresses[].company` | body | `string` | no | — |
| `addresses[].phone` | body | `string` | no | — |
| `addresses[].line_1` | body | `string` | no | — |
| `addresses[].line_2` | body | `string` | no | — |
| `addresses[].city` | body | `string` | no | — |
| `addresses[].state` | body | `string` | no | — |
| `addresses[].zip` | body | `string` | no | — |
| `addresses[].country` | body | `string` | no | — |
