# Add domain to redirect_uri whitelist with Neon

Adds trusted redirect URI domain in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/auth/domains`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Add domain to redirect_uri whitelist](https://api-docs.neon.tech/reference/addneonauthdomaintoredirecturiwhitelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `domain` | body | `string` | yes | Neon API parameter domain |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
