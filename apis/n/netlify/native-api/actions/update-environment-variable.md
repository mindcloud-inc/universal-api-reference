# Update Environment Variable with Netlify

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:account_id/env/:key`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Update Environment Variable](https://open-api.netlify.com/#operation/updateEnvVar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | — |
| `key` | path | `string` | yes | The existing environment variable key name (case-sensitive). |
| `site_id` | query | `string` | no | Update an environment variable set on this site. |
| `new_key` | body | `string` | no | The existing or new name of the key, if you wish to rename it. |
| `scopes` | body | `list<string>` | no | The scopes that this environment variable is set to. Accepted values: `builds`, `functions`, `post-processing`, `runtime`. |
| `values[]` | body | `array<object>` | no | — |
| `values[].id` | body | `string` | no | — |
| `values[].value` | body | `string` | no | — |
| `values[].context` | body | `list<string>` | no | Accepted values: `all`, `branch-deploy`, `deploy-preview`, `dev`, `dev-server`, `production`. |
| `context_parameter` | body | `string` | no | — |
| `is_secret` | body | `boolean` | no | Secret values are only readable by code running on Netlify's systems. |
