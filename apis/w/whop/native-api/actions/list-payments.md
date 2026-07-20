# List Payments with Whop

Retrieves payments from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/payments`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Payments](https://docs.whop.com/api-reference/payments/list-payments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list payments for. |
