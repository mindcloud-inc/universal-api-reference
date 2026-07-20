# Download Invoice PDF with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/invoice/:invitation_key/download`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Download Invoice PDF](https://api-docs.invoicing.co/#tag/invoices/operation/downloadInvoiceByInvitation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invitation_key` | path | `string` | yes | The invoice invitation key used for PDF download. |
