# Add a OAuth provider with Neon

Adds an OAuth provider in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/auth/oauth_providers`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Add a OAuth provider](https://api-docs.neon.tech/reference/addneonauthoauthprovider)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `id` | body | `list` | yes | Neon API parameter id Accepted values: `0`, `1`, `2`, `3`. |
| `client_id` | body | `string` | no | Neon API parameter client_id |
| `client_secret` | body | `string` | no | Neon API parameter client_secret |
| `microsoft_tenant_id` | body | `string` | no | Neon API parameter microsoft_tenant_id |
