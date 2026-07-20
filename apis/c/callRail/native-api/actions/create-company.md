# Create Company with CallRail

Creates a company in CallRail.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/a/:account_id/companies.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Create Company](https://apidocs.callrail.com/#creating-a-company)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `time_zone` | body | `string` | yes |
| `swap_ppc_override` | body | `boolean` | no |
| `swap_landing_override` | body | `boolean` | no |
| `callscribe_enabled` | body | `boolean` | no |
