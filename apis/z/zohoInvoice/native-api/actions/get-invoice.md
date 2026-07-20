# Get Invoice with Zoho Invoice

Retrieves an invoice from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:invoice_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Get Invoice](https://www.zoho.com/invoice/api/v3/invoices/#get-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `invoice_id` | path | `string` | yes | Unique identifier of the invoice. |
| `print` | query | `boolean` | no | Print the exported pdf. |
| `accept` | query | `list<string>` | no | Get the invoice in json, pdf, or html. Default format is json. Accepted values: `html`, `json`, `pdf`. |
