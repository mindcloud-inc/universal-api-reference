# Get Personal Access Tokens with Dremio

Retrieves personal access tokens for a Dremio user.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:user_id/token`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Personal Access Tokens](https://docs.dremio.com/dremio-cloud/api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | path | `string` | yes |
