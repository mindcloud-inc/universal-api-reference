# Approve Receipt with Aspire

Approves an existing Aspire receipt and can optionally receive it at the same time. This is the only post-create update path for a receipt. At approve time, the only receipt fields that can be added or changed are the vendor invoice number and vendor invoice date. No other receipt field can be edited through this action, including notes, extra costs or freight, receipt items, received date, vendor, branch, or work ticket. If the user asks to change a non-invoice-metadata field on an existing receipt, surface that limitation upfront and offer the available path of recreating the receipt with the corrected values.

## Endpoint

- **Method:** `POST`
- **Path:** `Receipts/Approve`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Approve Receipt](https://guide.youraspire.com/apidocs/receiptsapprove)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ReceiptID` | body | `list<number>` | no |
| `Receive` | body | `boolean` | no |
| `VendorInvoiceNum` | body | `string` | no |
| `VendorInvoiceDate` | body | `string` | no |
