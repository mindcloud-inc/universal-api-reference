# List Preview Deploy Keys with Convex

Retrieves preview deploy keys from a Convex project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/list_preview_deploy_keys`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [List Preview Deploy Keys](https://docs.convex.dev/management-api/list-preview-deploy-keys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Convex project ID. |
