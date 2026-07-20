# Create Supplier Invoice with Ascora

Creates a new supplier invoice in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/SupplierInvoices/SupplierInvoice`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Supplier Invoice](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=57)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingNumber` | body | `string` | yes | Supplier invoice number or credit note number. |
| `invoiceDate` | body | `date` | yes | Date associated with the supplier invoice. |
| `dueDate` | body | `date` | yes | Date on which the supplier invoice is due. |
| `supplier.name` | body | `string` | yes | Name of the supplier linked to the invoice. |
| `Lines[].description` | body | `string` | yes | Description for a supplier invoice line. |
| `Lines[].partNumber` | body | `string` | no | Part number for a supplier invoice line. |
| `Lines[].Quantity` | body | `number` | yes | Quantity for a supplier invoice line. |
| `Lines[].TotalAmountExTax` | body | `number` | yes | Total ex-tax amount for a supplier invoice line. |
| `reference` | body | `string` | no | Purchase order or job number associated with the supplier invoice. |
| `type` | body | `string` | no | Use INVOICE to create a supplier invoice or CREDIT to create a credit note. |
