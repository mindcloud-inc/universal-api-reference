# Create Workspace with Postman

Creates a new workspace in Postman.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Create Workspace](https://www.postman.com/postman/utility-flows/request/bl962uv/create-a-workspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace.name` | body | `string` | yes |
| `workspace.type` | body | `string` | yes |
