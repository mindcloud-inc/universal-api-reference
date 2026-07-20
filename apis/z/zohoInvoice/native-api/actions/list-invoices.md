# List Invoices with Zoho Invoice

Retrieves invoices from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [List Invoices](https://www.zoho.com/invoice/api/v3/invoices/#list-invoices)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `invoice_number` | query | `string` | no | An unique number given to the invoice. Maximum length [100] |
| `item_name` | query | `string` | no | item name. Variants: item_name_startswith and item_name_contains. Maximum length [100] |
| `item_id` | query | `string` | no | Unique item id. |
| `item_description` | query | `string` | no | Search invoices by item description. Variants: item_description_startswith and item_description_contains. Maximum length [100] |
| `reference_number` | query | `string` | no | The reference number of the invoice |
| `customer_name` | query | `string` | no | The name of the customer. Maximum length [100] |
| `recurring_invoice_id` | query | `string` | no | ID of the recurring invoice from which the invoice is created. |
| `email` | query | `string` | no | Contact email ID. Maximum length [100] |
| `total` | query | `string` | no | The total amount to be paid |
| `balance` | query | `string` | no | The unpaid amount |
| `custom_field` | query | `string` | no | Custom fields for invoice. Variants: custom_field_startswith and custom_field_contains |
| `date` | query | `date` | no | Invoice date. Date format yyyy-mm-dd. Variants: due_date_start, due_date_end, due_date_before, due_date_after. |
| `due_date` | query | `date` | no | Due date of the invoices. Date format yyyy-mm-dd. Variants: due_date_start, due_date_end, due_date_before, due_date_after. |
| `status` | query | `list<string>` | no | Search invoices by invoice status. Allowed values: sent, draft, overdue, paid, void, unpaid, partially_paid, viewed. Accepted values: `draft`, `overdue`, `paid`, `partially_paid`, `sent`, `unpaid`, `viewed`, `void`. |
| `customer_id` | query | `string` | no | ID of the customer to whom the invoice is created. |
| `filter_by` | query | `list<string>` | no | Filter invoices by any status or payment expected date. Accepted values: `Date.PaymentExpectedDate`, `Status.All`, `Status.Draft`, `Status.OverDue`, `Status.Paid`, `Status.PartiallyPaid`, `Status.Sent`, `Status.Unpaid`, `Status.Viewed`, `Status.Void`. |
| `search_text` | query | `string` | no | Search invoices by invoice number, purchase order, or customer name. Maximum length [100] |
| `zcrm_potential_id` | query | `number` | no | Potential ID of a Deal in CRM. |
