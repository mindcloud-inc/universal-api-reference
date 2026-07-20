# Delete domain from redirect_uri whitelist with Neon

Deletes a domain from the redirect URI whitelist in Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/domains`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete domain from redirect_uri whitelist](https://api-docs.neon.tech/reference/deletebranchneonauthtrusteddomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
| `domains[]` | body | `array<object>` | yes | Neon API parameter domains |
