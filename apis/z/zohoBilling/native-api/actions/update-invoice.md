# Update Invoice with Zoho Billing

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:invoice_id`
- **Base URL:** `{api_domain}/billing/v1`
- **Official documentation:** [Update Invoice](https://www.zoho.com/billing/api/v1/invoices/#update-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes | Unique identifier of the invoice. |
| `ignore_auto_number_generation` | query | `boolean` | no | When true, Zoho expects you to provide the invoice number explicitly. |
