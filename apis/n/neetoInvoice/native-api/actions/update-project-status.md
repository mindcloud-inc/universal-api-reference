# Update Project Status with NeetoInvoice

Updates a project status in NeetoInvoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/update_status`
- **Base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`
- **Official documentation:** [Update Project Status](https://apidocs.neetoinvoice.com/api-reference/projects/update-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | no | Project identifier whose status will be updated. |
| `status` | body | `string` | no | New project status. |
