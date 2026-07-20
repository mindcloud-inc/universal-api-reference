# Update Workflow User Permissions with SigningHub

Updates workflow user permissions in SigningHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/packages/:packageId/workflow/:order/permissions`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Update Workflow User Permissions](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_WorkflowPermission_UpdateWorkflowPermissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package whose workflow permissions should be updated. |
| `order` | path | `number` | yes | The recipient order whose permissions should be updated. |
| `apply_to_all` | body | `boolean` | yes | Whether to apply the permissions to all workflow users. |
| `permissions.print` | body | `boolean` | no | Whether the recipient can print the document. |
| `permissions.download` | body | `boolean` | no | Whether the recipient can download the document. |
| `add_text` | body | `boolean` | no | Whether the recipient can add text fields. |
| `change_recipients` | body | `boolean` | no | Whether the recipient can change remaining recipients. |
| `add_attachment` | body | `boolean` | no | Whether the recipient can add attachments. |
