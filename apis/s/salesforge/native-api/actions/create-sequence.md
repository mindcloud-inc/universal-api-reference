# Create Sequence with Salesforge

Creates a sequence in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Create Sequence](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID from the Salesforge workspace URL or List Workspaces action. |
| `name` | body | `string` | yes | Name of the sequence to create. |
| `productId` | body | `string` | yes | Product ID to associate with the sequence. |
| `language` | body | `string` | yes | Language used by the sequence. |
| `timezone` | body | `string` | yes | IANA timezone for the sequence. |
