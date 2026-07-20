# Update Workspace with DynaPictures

Updates an existing workspace in DynaPictures.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workspaces/:id`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Update Workspace](https://dynapictures.com/docs/#update-workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | ID of the workspace to update. |
| `name` | body | `string` | yes | New name for the workspace. |
