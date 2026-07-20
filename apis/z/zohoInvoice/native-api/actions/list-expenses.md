# List Expenses with Zoho Invoice

Retrieves expenses from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/expenses`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [List Expenses](https://www.zoho.com/invoice/api/v3/expenses/#list-expenses)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `search_text` | query | `string` | no | Search expenses by account name, description, customer name, or vendor name. |
| `reference_number` | query | `string` | no | Search expenses by reference number. |
| `date` | query | `date` | no | Search expenses by expense date. |
| `status` | query | `string` | no | Search expenses by expense status. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `amount` | query | `number` | no | Search expenses by amount. |
| `account_name` | query | `string` | no | Search expenses by expense account name. |
| `customer_name` | query | `string` | no | Search expenses by customer name. |
| `sort_column` | query | `string` | no | Sort expenses. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `filter_by` | query | `string` | no | Filter expenses by expense status. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
