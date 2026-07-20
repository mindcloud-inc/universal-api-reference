# Get Invoice with MILKEE

Retrieves an invoice from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/invoices/:invoiceId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Invoice](https://apidocs.milkee.ch/api/resources/invoices.html#einzelne-rechnung-abrufen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `invoice_id` | path | `string` | yes | The numeric MILKEE invoice ID used in the request path. |
