# List Labels with ContentStudio

Retrieves labels for a workspace from ContentStudio.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace_id/labels`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [List Labels](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of items per page. |
| `search` | query | `string` | no | Search term. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
