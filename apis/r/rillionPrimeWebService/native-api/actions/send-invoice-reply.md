# Send Invoice Reply with Rillion Prime Web Service

Confirm back to Prime how an exported invoice was processed in the ERP.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceReceipt` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, InvoiceReceipt section. |
| `InvoiceReceipt.InvoiceSeries` | body | `string` | yes | Invoice series |
| `InvoiceReceipt.InvoiceNo` | body | `number` | yes | Invoice number |
| `InvoiceReceipt.Status` | body | `number` | yes | The same status as the invoice had when it was exported from Prime |
| `InvoiceReceipt.ArrivalAccountCodingDate` | body | `date` | no | Accounting date for preliminary recording in ERP |
| `InvoiceReceipt.VoucherSeries` | body | `string` | no | Voucher series in ERP |
| `InvoiceReceipt.VoucherNo` | body | `number` | no | Voucher number in ERP |
| `InvoiceReceipt.QueueStatus` | body | `number` | yes | Queue status: 1=Correct; 2=Error |
| `InvoiceReceipt.ErrorText` | body | `string` | no | Error text if QueueStatus=2 |
| `InvoiceReceipt.InvoiceExternalId` | body | `string` | no | — |
| `InvoiceReceipt.InvoiceExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
