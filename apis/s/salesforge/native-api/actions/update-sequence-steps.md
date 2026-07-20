# Update Sequence Steps with Salesforge

Updates sequence steps in Salesforge.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/steps`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Update Sequence Steps](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to update steps for. |
| `steps[]` | body | `array<object>` | yes | Array of sequence steps to update. |
