# Update Sequence with Salesforge

Updates a sequence in Salesforge.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Update Sequence](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to update. |
| `name` | body | `string` | no | Updated name for the sequence. |
| `productId` | body | `string` | no | Updated product ID for the sequence. |
| `language` | body | `string` | no | Updated language for the sequence. |
| `timezone` | body | `string` | no | Updated timezone for the sequence. |
| `openTrackingEnabled` | body | `boolean` | no | Whether open tracking is enabled. |
| `clickTrackingEnabled` | body | `boolean` | no | Whether click tracking is enabled. |
