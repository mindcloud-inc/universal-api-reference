# Send Sales Invoice with MoneyBird

Sends an existing sales invoice from MoneyBird.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:administrationId/sales_invoices/:salesInvoiceId/send_invoice.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Send Sales Invoice](https://developer.moneybird.com/api/sales-invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `salesInvoiceId` | path | `string` | yes | Moneybird sales invoice ID. |
