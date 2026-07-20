# Get all plugin configurations with Neon

Retrieves Neon Auth plugin configurations from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/plugins`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get all plugin configurations](https://api-docs.neon.tech/reference/getneonauthpluginconfigs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
