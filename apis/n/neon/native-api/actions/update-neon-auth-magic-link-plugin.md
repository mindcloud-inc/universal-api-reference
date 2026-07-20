# Update magic link plugin configuration with Neon

Updates magic link plugin configuration in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/plugins/magic-link`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update magic link plugin configuration](https://api-docs.neon.tech/reference/updateneonauthmagiclinkplugin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `enabled` | body | `boolean` | no | Neon API parameter enabled |
| `expires_in` | body | `number` | no | Neon API parameter expires_in |
| `disable_sign_up` | body | `boolean` | no | Neon API parameter disable_sign_up |
