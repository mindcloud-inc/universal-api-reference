# Create Workspace with Rossum

Creates a new workspace in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Workspace](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the workspace to create. |
| `organization` | body | `string` | yes | Organization URL that owns the workspace. |
| `autopilot` | body | `boolean` | no | Whether autopilot should be enabled for the workspace. |
