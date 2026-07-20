# Get advisor issues with Neon

Retrieves advisor issues for a project from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/advisors`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get advisor issues](https://api-docs.neon.tech/reference/getprojectadvisorsecurityissues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | query | `string` | no | Neon API parameter branch_id |
| `database_name` | query | `string` | no | Neon API parameter database_name |
| `category` | query | `list` | no | Neon API parameter category Accepted values: `0`, `1`. |
| `min_severity` | query | `list` | no | Neon API parameter min_severity Accepted values: `0`, `1`, `2`. |
