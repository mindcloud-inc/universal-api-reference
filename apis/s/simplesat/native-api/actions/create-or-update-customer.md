# Create or Update Customer with Simplesat

Creates or updates a customer in Simplesat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/customers`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Create or Update Customer](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `external_id` | body | `string` | no |
| `email` | body | `string` | no |
| `name` | body | `string` | no |
| `company` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
| `custom_attributes` | body | `object` | no |
