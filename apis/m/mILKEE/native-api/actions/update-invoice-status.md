# Update Invoice Status with MILKEE

Updates an invoice status in MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/invoices/:invoiceId/mark-as`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Invoice Status](https://apidocs.milkee.ch/api/resources/invoices.html#status-andern-mark-as)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bank_account_id` | query | `number` | no | Bank account ID for payment booking. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `createEntry` | query | `boolean` | no | Create an accounting entry when marking the invoice as paid. |
| `invoice_id` | path | `string` | yes | The numeric MILKEE invoice ID used in the request path. |
| `paidDate` | query | `string` | no | Payment date for the paid transition. |
| `status` | query | `string` | yes | Target invoice status transition. |
