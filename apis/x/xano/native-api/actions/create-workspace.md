# Create Workspace with Xano

Creates a new workspace in Xano.

## Endpoint

- **Method:** `POST`
- **Path:** `/api%3Ameta/workspace`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Create Workspace](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Workspace description. |
| `name` | body | `string` | yes | Workspace name. |
