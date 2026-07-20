# List Invoices with Ablefy

Retrieves invoices from Ablefy.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/invoices`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [List Invoices](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date_from` | query | `date` | no |
| `date_to` | query | `date` | no |
| `predefined_date_range` | query | `string` | no |
| `invoice_state` | query | `string` | no |
| `payment_state` | query | `string` | no |
| `product_id` | query | `number` | no |
