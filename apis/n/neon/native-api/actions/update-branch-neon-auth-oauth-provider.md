# Update OAuth provider with Neon

Updates an OAuth provider in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/oauth_providers/:oauth_provider_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update OAuth provider](https://api-docs.neon.tech/reference/updatebranchneonauthoauthprovider)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `oauth_provider_id` | path | `list` | yes | Neon API parameter oauth_provider_id Accepted values: `0`, `1`, `2`, `3`. |
| `client_id` | body | `string` | no | Neon API parameter client_id |
| `client_secret` | body | `string` | no | Neon API parameter client_secret |
| `microsoft_tenant_id` | body | `string` | no | Neon API parameter microsoft_tenant_id |
