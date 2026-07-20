# Get list of all workspaces with Affinda

Retrieves all accessible workspaces from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/workspaces`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get list of all workspaces](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter by name. |
| `organization` | query | `string` | yes | Filter by organization. |
