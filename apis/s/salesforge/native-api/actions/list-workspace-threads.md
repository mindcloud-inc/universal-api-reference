# List Workspace Threads with Salesforge

Retrieves workspace threads from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/threads`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [List Workspace Threads](https://api.salesforge.ai/public/v2/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes |
| `mailbox_ids[]` | query | `array<string>` | no |
| `agent_ids[]` | query | `array<string>` | no |
| `sequence_ids[]` | query | `array<string>` | no |
