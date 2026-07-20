# List Payments with Alegra

Retrieves payments from your Alegra account.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [List Payments](https://developer.alegra.com/reference/get_payments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start` | query | `number` | no |
| `limit` | query | `number` | no |
| `order_direction` | query | `string` | no |
| `order_field` | query | `string` | no |
| `type` | query | `string` | no |
| `metadata` | query | `boolean` | no |
| `client_id` | query | `number` | no |
| `conciliation_id` | query | `number` | no |
| `id` | query | `string` | no |
| `includeUnconciliated` | query | `boolean` | no |
| `fields` | query | `string` | no |
