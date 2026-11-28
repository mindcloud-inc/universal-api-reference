# Create Sales Invoice with MoneyBird

Creates a new sales invoice in MoneyBird.

## Endpoint

- **Method:** `POST`
- **Path:** `/:administrationId/sales_invoices.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Create Sales Invoice](https://developer.moneybird.com/api/sales-invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `sales_invoice` | body | `object` | no | — |
| `sales_invoice.contact_id` | body | `string` | yes | — |
| `salesInvoice.reference` | body | `string` | no | — |
| `salesInvoice.currency` | body | `string` | no | — |
| `sales_invoice.prices_are_incl_tax` | body | `boolean` | no | — |
| `sales_invoice.details_attributes[]` | body | `array<object>` | no | — |
| `sales_invoice.details_attributes[].description` | body | `string` | no | — |
| `sales_invoice.details_attributes[].amount` | body | `number` | no | — |
| `sales_invoice.details_attributes[].price` | body | `number` | no | — |
| `sales_invoice.details_attributes[].tax_rate_id` | body | `string` | no | — |
| `sales_invoice.details_attributes[].ledger_account_id` | body | `string` | no | — |
