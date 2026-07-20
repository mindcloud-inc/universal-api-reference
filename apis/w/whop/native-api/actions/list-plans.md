# List Plans with Whop

Retrieves subscription plans from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/plans`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Plans](https://docs.whop.com/api-reference/plans/list-plans)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list plans for. |
