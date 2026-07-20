# Delete Personal Access Token By ID with Dremio

Deletes a personal access token from Dremio by ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/user/:user_id/token/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Delete Personal Access Token By ID](https://docs.dremio.com/dremio-cloud/api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `user_id` | path | `string` | yes |
