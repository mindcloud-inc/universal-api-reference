# Create Customer with Clockodo

Creates a customer in your Clockodo account.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Create Customer](https://www.clockodo.com/en/api/customers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `boolean` | no |
| `billable_default` | body | `boolean` | no |
| `name` | body | `string` | yes |
| `note` | body | `string` | no |
| `number` | body | `string` | no |
