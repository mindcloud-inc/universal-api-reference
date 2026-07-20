# Update Expense with Zoho Invoice

Updates an expense in Zoho Invoice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/expenses/:expense_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Update Expense](https://www.zoho.com/invoice/api/v3/expenses/#update-an-expense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `expense_id` | path | `string` | yes | Unique identifier of the expense. |
| `amount` | body | `number` | yes | Total expense value. |
| `reference_number` | body | `string` | yes | Reference number of the expense. |
| `date` | body | `date` | no | Date of the expense. |
| `description` | body | `string` | no | Description of the expense. |
| `account_id` | body | `string` | no | ID of the expense account. |
| `is_billable` | body | `boolean` | no | Check if an expense is billable. |
| `customer_id` | body | `string` | no | ID of the expense account. |
| `project_id` | body | `string` | no | ID of the project associated with the customer. |
