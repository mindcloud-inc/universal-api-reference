# Update Company with CallRail

Updates a company in CallRail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/a/:account_id/companies/:company_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Update Company](https://apidocs.callrail.com/#updating-a-company)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `company_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `time_zone` | body | `string` | no |
| `swap_ppc_override` | body | `boolean` | no |
| `swap_landing_override` | body | `boolean` | no |
| `callscribe_enabled` | body | `boolean` | no |
