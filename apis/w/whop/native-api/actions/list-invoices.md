# List Invoices with Whop

Retrieves invoices from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/invoices`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Invoices](https://docs.whop.com/api-reference/invoices/list-invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list invoices for. |
