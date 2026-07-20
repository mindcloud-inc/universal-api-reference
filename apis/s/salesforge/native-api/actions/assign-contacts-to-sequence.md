# Assign Contacts To Sequence with Salesforge

Assigns contacts to a sequence in Salesforge.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Assign Contacts To Sequence](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to assign contacts to. |
| `contactIds[]` | body | `array<string>` | yes | Contact IDs to assign to the sequence. |
