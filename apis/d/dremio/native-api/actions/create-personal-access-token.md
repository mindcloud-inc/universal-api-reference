# Create Personal Access Token with Dremio

Creates a new personal access token in Dremio.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/:user_id/token`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create Personal Access Token](https://docs.dremio.com/dremio-cloud/api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label` | body | `string` | yes |
| `user_id` | path | `string` | yes |
