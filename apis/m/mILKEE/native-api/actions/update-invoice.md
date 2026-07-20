# Update Invoice with MILKEE

Updates an existing invoice in MILKEE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:companyId/invoices/:invoiceId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Invoice](https://apidocs.milkee.ch/api/resources/invoices.html#rechnung-aktualisieren)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer_id` | body | `number` | no | Customer ID for the invoice. |
| `discount_rate` | body | `number` | no | Overall discount percentage. |
| `invoice_id` | path | `string` | yes | The numeric MILKEE invoice ID used in the request path. |
| `payable_until` | body | `string` | no | Invoice due date. |
| `positions` | body | `string` | no | Invoice positions as a JSON string. |
| `remarks` | body | `string` | no | Bottom remarks. |
| `tax_rate_id` | body | `number` | no | Tax rate ID. |
| `title` | body | `string` | no | Invoice title. |
