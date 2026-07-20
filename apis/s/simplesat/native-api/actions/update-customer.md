# Update Customer with Simplesat

Updates an existing customer in Simplesat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/customers/:customer_id`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Update Customer](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The ID of the customer to update |
| `external_id` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `custom_attributes` | body | `object` | no | — |
