# Get details of Neon Auth for the branch with Neon

Retrieves Neon Auth details for the branch from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get details of Neon Auth for the branch](https://api-docs.neon.tech/reference/getneonauth)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
