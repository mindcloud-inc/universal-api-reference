# Update Sales Invoice with MoneyBird

Updates an existing sales invoice in MoneyBird.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:administrationId/sales_invoices/:salesInvoiceId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Update Sales Invoice](https://developer.moneybird.com/api/sales-invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `salesInvoiceId` | path | `string` | yes | Moneybird sales invoice ID. |
