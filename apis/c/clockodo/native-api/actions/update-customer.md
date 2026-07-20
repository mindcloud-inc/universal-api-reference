# Update Customer with Clockodo

Updates a customer in your Clockodo account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:id`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Update Customer](https://www.clockodo.com/en/api/customers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `boolean` | no |
| `billable_default` | body | `boolean` | no |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `note` | body | `string` | no |
| `number` | body | `string` | no |
