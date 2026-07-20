# List domains in redirect_uri whitelist with Neon

Retrieves redirect URI whitelist domains from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/domains`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List domains in redirect_uri whitelist](https://api-docs.neon.tech/reference/listbranchneonauthtrusteddomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
