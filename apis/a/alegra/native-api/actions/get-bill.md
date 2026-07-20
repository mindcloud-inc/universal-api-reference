# Get Bill with Alegra

Retrieves a purchase bill from Alegra.

## Endpoint

- **Method:** `GET`
- **Path:** `/bills/:id`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Get Bill](https://developer.alegra.com/reference/get_bills-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `fields` | query | `string` | no |
| `includeVoidPayments` | query | `string` | no |
