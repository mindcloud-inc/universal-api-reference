# Update allow localhost with Neon

Updates localhost allow setting in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/allow_localhost`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update allow localhost](https://api-docs.neon.tech/reference/updateneonauthallowlocalhost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `allow_localhost` | body | `boolean` | yes | Neon API parameter allow_localhost |
