# List Bills with Alegra

Retrieves purchase bills from your Alegra account.

## Endpoint

- **Method:** `GET`
- **Path:** `/bills`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [List Bills](https://developer.alegra.com/reference/get_bills)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `metadata` | query | `boolean` | no |
| `start` | query | `number` | no |
| `limit` | query | `number` | no |
| `order_direction` | query | `string` | no |
| `order_field` | query | `string` | no |
| `billNumber` | query | `string` | no |
| `client_name` | query | `string` | no |
| `date` | query | `string` | no |
| `dueDate` | query | `string` | no |
| `status` | query | `string` | no |
| `item_id` | query | `number` | no |
| `client_id` | query | `number` | no |
| `provider_name` | query | `string` | no |
| `uuid` | query | `string` | no |
| `purchaseOrder_id` | query | `number` | no |
| `type` | query | `string` | no |
