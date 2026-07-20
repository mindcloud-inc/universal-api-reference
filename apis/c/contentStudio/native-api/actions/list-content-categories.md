# List Content Categories with ContentStudio

Retrieves content categories for a workspace from ContentStudio.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace_id/content-categories`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [List Content Categories](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of items per page. |
| `search` | query | `string` | no | Search term. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
