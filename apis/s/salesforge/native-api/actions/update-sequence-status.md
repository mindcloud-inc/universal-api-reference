# Update Sequence Status with Salesforge

Updates sequence status in Salesforge.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/status`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Update Sequence Status](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to update. |
| `status` | body | `string` | yes | New sequence status. |
