# Create Invoice with Zoho Billing

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `{api_domain}/billing/v1`
- **Official documentation:** [Create Invoice](https://www.zoho.com/billing/api/v1/invoices/#create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `send` | query | `boolean` | no | Send the invoice to the associated contact people after creation. |
| `ignore_auto_number_generation` | query | `boolean` | no | When true, Zoho expects you to provide the invoice number explicitly. |
