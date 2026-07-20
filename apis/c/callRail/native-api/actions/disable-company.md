# Disable Company with CallRail

Disables a company in CallRail.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/a/:account_id/companies/:company_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Disable Company](https://apidocs.callrail.com/#disabling-a-company)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `company_id` | path | `string` | yes |
