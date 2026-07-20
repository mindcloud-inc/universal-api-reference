# List Post Comments with ContentStudio

Retrieves comments for a post from ContentStudio.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace_id/posts/:post_id/comments`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [List Post Comments](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of items per page. |
| `post_id` | path | `string` | yes | ContentStudio post ID. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
