# Delete Sequence with Salesforge

Deletes a sequence from Salesforge.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Delete Sequence](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to delete. |
