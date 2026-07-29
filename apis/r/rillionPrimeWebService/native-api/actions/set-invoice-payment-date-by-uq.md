# Set Invoice Payment Date by UQ with Rillion Prime Web Service

Register the payment date for an invoice identified by its unique key.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Company` | body | `list<string>` | yes | Company ID of the invoice. |
| `Supplier` | body | `string` | yes | Supplier ID of the invoice. |
| `SupplierInvoiceNo` | body | `string` | yes | Supplier invoice number. |
| `PaymentDate` | body | `date` | yes | Payment date to register. |
| `Note` | body | `string` | no | Optional note stored with the payment date. |
