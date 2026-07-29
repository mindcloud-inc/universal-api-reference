# Count Account Coded Invoices with Rillion Prime Web Service

Count how many times an invoice has been account coded.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceSeries` | body | `string` | yes | Invoice series of the invoice. |
| `InvoiceNo` | body | `number` | yes | Invoice number of the invoice. |
