# Get allow localhost with Neon

Retrieves localhost allow setting from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/allow_localhost`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get allow localhost](https://api-docs.neon.tech/reference/getneonauthallowlocalhost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
