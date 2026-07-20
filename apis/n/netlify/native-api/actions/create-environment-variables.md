# Create Environment Variables with Netlify

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/env`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Create Environment Variables](https://open-api.netlify.com/#operation/createEnvVars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | — |
| `site_id` | query | `string` | no | Create the environment variables on this site instead of at the account level. |
| `[]` | body | `array<object>` | no | The environment variables to create. |
| `[].key` | body | `string` | no | — |
| `[].scopes` | body | `list<string>` | no | The scopes that this environment variable is set to. Accepted values: `builds`, `functions`, `post-processing`, `runtime`. |
| `[].values[]` | body | `array<object>` | no | — |
| `[].values[].id` | body | `string` | no | — |
| `[].values[].value` | body | `string` | no | — |
| `[].values[].context` | body | `list<string>` | no | Accepted values: `all`, `branch-deploy`, `deploy-preview`, `dev`, `dev-server`, `production`. |
| `context_parameter` | body | `string` | no | — |
| `is_secret` | body | `boolean` | no | Secret values are only readable by code running on Netlify's systems. |
