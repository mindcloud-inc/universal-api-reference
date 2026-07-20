# Create Invoice with Tidely

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/open-api/invoices`
- **Base URL:** `https://api.tidely.com`
- **Official documentation:** [Create Invoice](https://api.tidely.com/tidely-open-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactName` | body | `string` | no | Invoice contact name. |
| `dueDate` | body | `string` | no | Due date in YYYY-MM-DD format. |
| `invoiceDate` | body | `string` | no | Invoice date in YYYY-MM-DD format. |
| `invoiceId` | body | `string` | no | External invoice identifier. |
| `invoiceNumber` | body | `string` | no | Invoice number. |
| `invoiceStatus` | body | `string` | no | Tidely invoice status. |
| `invoiceType` | body | `string` | no | Tidely invoice type. |
| `openAmount` | body | `string` | no | Remaining open amount. |
| `totalGrossAmount` | body | `string` | no | Gross invoice amount. |
