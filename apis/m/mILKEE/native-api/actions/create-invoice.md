# Create Invoice with MILKEE

Creates a new invoice in MILKEE.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/invoices`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Create Invoice](https://apidocs.milkee.ch/api/resources/invoices.html#neue-rechnung-erstellen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer_id` | body | `number` | yes | Customer ID for the invoice. |
| `date` | body | `string` | no | Invoice date. |
| `lang` | body | `string` | no | Document language: de, en, fr, or it. |
| `payable_until` | body | `string` | no | Invoice due date. |
| `positions` | body | `string` | yes | Invoice positions as a JSON string. |
| `remarks` | body | `string` | no | Bottom remarks. |
| `tax_rate_id` | body | `number` | no | Tax rate ID. |
| `title` | body | `string` | no | Invoice title. |
