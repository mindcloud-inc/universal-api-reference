# List OAuth providers for neon auth for a branch with Neon

Retrieves OAuth providers for the branch from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/oauth_providers`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List OAuth providers for neon auth for a branch](https://api-docs.neon.tech/reference/listbranchneonauthoauthproviders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
