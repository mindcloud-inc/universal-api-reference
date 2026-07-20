# Get Sales Invoice with MoneyBird

Retrieves a sales invoice from MoneyBird.

## Endpoint

- **Method:** `GET`
- **Path:** `/:administrationId/sales_invoices/:salesInvoiceId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Get Sales Invoice](https://developer.moneybird.com/api/sales-invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `salesInvoiceId` | path | `string` | yes | Moneybird sales invoice ID. |
