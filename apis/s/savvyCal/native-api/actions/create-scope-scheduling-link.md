# Create Scope Scheduling Link with SavvyCal

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scopes/:scope_slug/links`
- **Base URL:** `https://api.savvycal.com`
- **Official documentation:** [Create Scope Scheduling Link](https://developers.savvycal.com/api/create-scope-scheduling-link)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `scope_slug` | path | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `private_name` | body | `string` | no |
| `type` | body | `string` | no |
