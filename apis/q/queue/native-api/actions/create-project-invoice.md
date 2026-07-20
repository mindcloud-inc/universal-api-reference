# Create Project Invoice with Queue

Creates a new invoice for a Queue project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/invoices`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Create Project Invoice](https://docs.usequeue.com/api-reference/invoices/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `bill_to` | query | `string` | no |
| `address` | query | `string` | no |
| `tax` | query | `number` | no |
| `payment_terms` | query | `string` | no |
| `due` | query | `string` | no |
| `payment_method` | query | `string` | no |
| `invoice_number` | query | `number` | no |
| `currency` | query | `string` | no |
| `credit_type` | query | `boolean` | no |
