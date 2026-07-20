# Create Document with Grist

Creates a new document in Grist.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/docs`
- **Base URL:** `https://docs.getgrist.com/api`
- **Official documentation:** [Create Document](https://support.getgrist.com/api/#tag/docs/operation/createDoc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<number>` | yes | Workspace ID |
| `name` | body | `string` | yes | Document name |
| `isPinned` | body | `boolean` | no | Whether to pin the document |
