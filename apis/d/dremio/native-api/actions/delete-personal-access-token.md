# Delete Personal Access Token with Dremio

Deletes personal access tokens for a Dremio user.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/user/:user_id/token`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Delete Personal Access Token](https://docs.dremio.com/dremio-cloud/api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | path | `string` | yes |
