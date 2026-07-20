# List Invoices with Alegra

Retrieves sales invoices from your Alegra account.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [List Invoices](https://developer.alegra.com/reference/get_invoices)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start` | query | `number` | no |
| `limit` | query | `number` | no |
| `order_direction` | query | `string` | no |
| `order_field` | query | `string` | no |
| `metadata` | query | `boolean` | no |
| `id` | query | `string` | no |
| `date` | query | `string` | no |
| `dueDate` | query | `string` | no |
| `status` | query | `string` | no |
| `client_id` | query | `string` | no |
| `client_name` | query | `string` | no |
| `client_identification` | query | `string` | no |
| `numberTemplate_fullNumber` | query | `string` | no |
| `item_id` | query | `string` | no |
| `date_after` | query | `string` | no |
| `date_afterOrNow` | query | `string` | no |
| `date_before` | query | `string` | no |
| `date_beforeOrNow` | query | `string` | no |
| `dueDate_after` | query | `string` | no |
| `dueDate_afterOrNow` | query | `string` | no |
| `dueDate_before` | query | `string` | no |
| `dueDate_beforeOrNow` | query | `string` | no |
| `toReplace` | query | `boolean` | no |
| `download` | query | `boolean` | no |
| `downloadType` | query | `string` | no |
