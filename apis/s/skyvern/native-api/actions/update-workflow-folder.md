# Update Workflow Folder with Skyvern

Updates a workflow's folder assignment in Skyvern.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/workflows/:workflow_permanent_id/folder`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Update Workflow Folder](https://www.skyvern.com/docs/api-reference/workflows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | body | `string` | no | Folder ID to assign workflow to. Set to null to remove from folder. |
| `workflow_permanent_id` | path | `string` | yes | Workflow permanent ID |
