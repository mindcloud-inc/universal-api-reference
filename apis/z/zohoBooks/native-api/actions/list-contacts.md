# List Contacts with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [List Contacts](https://www.zoho.com/books/api/v3/contacts/#list-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_type` | query | `list` | no | Search contacts by contact type. Allowed values: customer or vendor. Accepted values: `customer`, `vendor`. |
| `contact_name` | query | `string` | no | Search contacts by contact name. |
| `email` | query | `string` | no | Search contacts by primary contact email. |
| `search_text` | query | `string` | no | Search contacts by contact name or notes. |
| `filter_by` | query | `list` | no | Filter contacts by documented contact or invoice status values. Accepted values: `Invoice.OverDue`, `Invoice.Unpaid`, `Status.Active`, `Status.All`, `Status.CreditLimitExceed`, `Status.Crm`, `Status.Duplicate`, `Status.Inactive`, `Status.PortalDisabled`, `Status.PortalEnabled`. |
| `sort_column` | query | `list` | no | Sort contacts by a supported column. Accepted values: `contact_name`, `created_time`, `email`, `first_name`, `last_modified_time`, `last_name`, `outstanding_receivable_amount`. |
