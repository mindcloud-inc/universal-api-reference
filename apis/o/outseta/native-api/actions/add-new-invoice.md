# Add New Invoice with Outseta

Creates a new invoice in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/invoices`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add New Invoice](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Subscription.Uid` | body | `string` | no |
| `InvoiceDate` | body | `string` | no |
| `InvoiceLineItems[].Description` | body | `string` | no |
| `InvoiceLineItems[].Amount` | body | `number` | no |
