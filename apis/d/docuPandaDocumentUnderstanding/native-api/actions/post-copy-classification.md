# Copy a Class to Another Workspace with DocuPanda - Document Understanding

Creates a class copy in another DocuPanda workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/copy/classification`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Copy a Class to Another Workspace](https://docs.docupipe.ai/reference/post_copy_classification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classId` | body | `string` | yes | Unique identifier of the class to copy. |
| `targetWorkspaceApiKey` | body | `string` | yes | API key of the target workspace. |
