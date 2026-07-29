# Set Invoice Payment Date with Rillion Prime Web Service

Register the payment date for an invoice in Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oInvoicePaymentDateItem` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, InvoicePaymentDate section. |
| `oInvoicePaymentDateItem.InvoiceSeries` | body | `string` | yes | Invoice series |
| `oInvoicePaymentDateItem.InvoiceNo` | body | `number` | yes | Invoice number |
| `oInvoicePaymentDateItem.PaymentDate` | body | `date` | yes | Payment date in ERP |
| `oInvoicePaymentDateItem.Note` | body | `string` | yes | Information about the payment e.g. check number. Information will be available on the invoice comment section. |
