# Create Expense with Zoho Invoice

Creates an expense in Zoho Invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/expenses`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Create Expense](https://www.zoho.com/invoice/api/v3/expenses/#create-an-expense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `amount` | body | `number` | yes | Total expense value. |
| `reference_number` | body | `string` | yes | Reference number of the expense. |
| `date` | body | `date` | no | Date of the expense. |
| `description` | body | `string` | no | Description of the expense. |
| `account_id` | body | `string` | no | ID of the expense account. |
| `is_billable` | body | `boolean` | no | Check if an expense is billable. |
| `customer_id` | body | `string` | no | ID of the expense account. |
| `project_id` | body | `string` | no | ID of the project associated with the customer. |
