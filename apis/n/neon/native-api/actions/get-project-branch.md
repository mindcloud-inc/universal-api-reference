# Retrieve branch details with Neon

Retrieves branch details from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve branch details](https://api-docs.neon.tech/reference/getprojectbranch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
