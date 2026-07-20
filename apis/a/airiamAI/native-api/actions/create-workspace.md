# Create Workspace with Airiam AI

Creates a new workspace in Airiam AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspaces`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [Create Workspace](https://docs.ai.airiam.com/reference/workspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Workspace name. |
| `description` | body | `string` | no | Workspace description. |
