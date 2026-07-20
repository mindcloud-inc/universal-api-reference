# List Company Users with Procore

Retrieves company users from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/companies/[:company_id]/users`
- **Base URL:** `https://api.procore.com`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | path | `string` | no |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
