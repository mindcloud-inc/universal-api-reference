# Set branch as default with Neon

Sets a branch as default in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/set_as_default`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Set branch as default](https://api-docs.neon.tech/reference/setdefaultprojectbranch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
