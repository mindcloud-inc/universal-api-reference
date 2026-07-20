# Update Service with Clockodo

Updates a service in your Clockodo account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/services/:id`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Update Service](https://www.clockodo.com/en/api/services/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `string` | no |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `note` | body | `string` | no |
| `number` | body | `string` | no |
