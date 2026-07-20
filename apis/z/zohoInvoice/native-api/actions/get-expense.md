# Get Expense with Zoho Invoice

Retrieves an expense from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/expenses/:expense_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Get Expense](https://www.zoho.com/invoice/api/v3/expenses/#get-an-expense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `expense_id` | path | `string` | yes | Unique identifier of the expense. |
