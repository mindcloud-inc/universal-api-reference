# List domains in redirect_uri whitelist with Neon

Retrieves trusted redirect URI domains from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/auth/domains`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List domains in redirect_uri whitelist](https://api-docs.neon.tech/reference/listneonauthredirecturiwhitelistdomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
