# Create Invoice with Refrens

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:urlKey/invoices`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Create Invoice](https://www.refrens.com/api/docs/invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billedTo` | body | `object` | yes | Customer billing object for the invoice. |
| `items[]` | body | `array<object>` | yes | Invoice line items array. |
| `invoiceNumber` | body | `string` | no | Optional invoice number. |
| `invoiceDate` | body | `date` | no | Invoice date. |
| `currency` | body | `string` | no | Invoice currency code. |
