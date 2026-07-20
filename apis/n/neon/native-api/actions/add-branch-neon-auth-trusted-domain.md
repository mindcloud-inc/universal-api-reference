# Add domain to redirect_uri whitelist with Neon

Adds a domain to the redirect URI whitelist in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/domains`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Add domain to redirect_uri whitelist](https://api-docs.neon.tech/reference/addbranchneonauthtrusteddomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `domain` | body | `string` | yes | Neon API parameter domain |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
