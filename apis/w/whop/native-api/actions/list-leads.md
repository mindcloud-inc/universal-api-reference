# List Leads with Whop

Retrieves leads from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/leads`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Leads](https://docs.whop.com/api-reference/leads/list-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list leads for. |
