# Get Invoice Image with Rillion Prime Web Service

Get the stored image files for one invoice.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceSeries` | body | `string` | yes | Invoice series of the invoice. |
| `InvoiceNo` | body | `number` | yes | Invoice number of the invoice. |
