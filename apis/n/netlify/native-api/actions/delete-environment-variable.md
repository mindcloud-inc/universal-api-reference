# Delete Environment Variable with Netlify

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts/:account_id/env/:key`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Delete Environment Variable](https://open-api.netlify.com/#operation/deleteEnvVar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | — |
| `key` | path | `string` | yes | The environment variable key (case-sensitive). |
| `site_id` | query | `string` | no | Delete the environment variable from this site only. |
