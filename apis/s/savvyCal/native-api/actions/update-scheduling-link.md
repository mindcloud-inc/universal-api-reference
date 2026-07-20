# Update Scheduling Link with SavvyCal

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/links/:link_id`
- **Base URL:** `https://api.savvycal.com`
- **Official documentation:** [Update Scheduling Link](https://developers.savvycal.com/api/update-scheduling-link)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `private_name` | body | `string` | no |
| `type` | body | `string` | no |
