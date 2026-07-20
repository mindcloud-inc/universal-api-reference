# Move Package To Folder with SigningHub

Moves a package to a folder in SigningHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/packages/:packageId/move_to`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Move Package To Folder](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Folder_MovePackage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package to move. |
| `folder_name` | body | `string` | yes | The destination custom or shared-space folder name. |
