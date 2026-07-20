# Delete Invoice with Tidely

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/open-api/invoices`
- **Base URL:** `https://api.tidely.com`
- **Official documentation:** [Delete Invoice](https://api.tidely.com/tidely-open-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactName` | body | `string` | no | Invoice contact name. |
| `invoiceId` | body | `string` | no | External invoice identifier to delete. |
| `invoiceNumber` | body | `string` | no | Invoice number. |
| `invoiceStatus` | body | `string` | no | Tidely invoice status. |
| `invoiceType` | body | `string` | no | Tidely invoice type. |
| `totalGrossAmount` | body | `string` | no | Gross invoice amount. |
