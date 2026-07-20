# Get Sequence Contacts Count with Salesforge

Retrieves a sequence contacts count from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/count`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Get Sequence Contacts Count](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to count contacts for. |
| `statuses` | query | `list<string>` | no | Only count contacts in the selected statuses. Send multiple values as a array. |
