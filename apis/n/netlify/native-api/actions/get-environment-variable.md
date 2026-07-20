# Get Environment Variable with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/env/:key`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Get Environment Variable](https://open-api.netlify.com/#operation/getEnvVar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | — |
| `key` | path | `string` | yes | The environment variable key (case-sensitive). |
| `site_id` | query | `string` | no | Return the environment variable for a specific site. |
