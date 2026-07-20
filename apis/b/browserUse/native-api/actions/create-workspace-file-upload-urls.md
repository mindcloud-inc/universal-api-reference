# Create Workspace File Upload URLs with Browser Use

Retrieves presigned upload URLs for workspace files from Browser Use.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspace_id/files/upload`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Create Workspace File Upload URLs](https://docs.browser-use.com/cloud/api-v3/workspaces/upload-workspace-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<object>` | yes | Files to upload. Each item should include the workspace-relative path or file metadata accepted by Browser Use. |
| `prefix` | query | `string` | no | Directory prefix to upload into, such as uploads/. |
| `workspace_id` | path | `string` | yes | Workspace ID. |
