# Delete OAuth provider with Neon

Deletes an OAuth provider from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/oauth_providers/:oauth_provider_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete OAuth provider](https://api-docs.neon.tech/reference/deletebranchneonauthoauthprovider)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `oauth_provider_id` | path | `list` | yes | Neon API parameter oauth_provider_id Accepted values: `0`, `1`, `2`, `3`. |
