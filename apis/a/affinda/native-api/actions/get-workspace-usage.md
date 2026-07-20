# Get usage by workspace with Affinda

Retrieves monthly credits usage for an Affinda workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/workspaces/:identifier/usage`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get usage by workspace](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | End date of the period to retrieve. Format: YYYY-MM |
| `identifier` | path | `string` | yes | Workspace's identifier |
| `start` | query | `string` | no | Start date of the period to retrieve. Format: YYYY-MM |
