# List branches with Neon

Retrieves branches from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List branches](https://api-docs.neon.tech/reference/listprojectbranches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `search` | query | `string` | no | Neon API parameter search |
| `sort_by` | query | `list` | no | Neon API parameter sort_by Accepted values: `0`, `1`, `2`. |
| `sort_order` | query | `list` | no | Neon API parameter sort_order Accepted values: `0`, `1`. |
