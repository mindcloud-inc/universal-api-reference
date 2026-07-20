# List Memberships with Whop

Retrieves memberships from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/memberships`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Memberships](https://docs.whop.com/api-reference/memberships/list-memberships)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list memberships for. |
