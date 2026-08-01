# Add Cash Receipts (SOAP) with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `/ws/AddCash_Receipts`
- **Base URL:** `{url}:8482/`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerCode` | body | `string` | no |
| `batchCode` | body | `string` | no |
| `transactionCode` | body | `string` | no |
| `referenceNumber` | body | `string` | no |
| `referenceDate` | body | `string` | no |
| `transactionAmount` | body | `string` | no |
| `abaNumber` | body | `string` | no |
| `invoiceNumber` | body | `string` | no |
| `invoiceType` | body | `string` | no |
| `paymentAmount` | body | `string` | no |
| `discountTaken` | body | `string` | no |
| `costCenterHeader` | body | `string` | no |
