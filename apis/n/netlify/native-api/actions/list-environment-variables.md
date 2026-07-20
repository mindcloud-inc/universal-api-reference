# List Environment Variables with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/env`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [List Environment Variables](https://open-api.netlify.com/#operation/getEnvVars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | — |
| `site_id` | query | `string` | no | Only return environment variables set on this site. |
| `context_name` | query | `list<string>` | no | Filter by deploy context. Accepted values: `all`, `branch-deploy`, `deploy-preview`, `dev`, `dev-server`, `production`. |
| `scope` | query | `list<string>` | no | Filter by scope. Accepted values: `builds`, `functions`, `post-processing`, `runtime`. |
