# Start Sequence Contact Validation with Salesforge

Starts sequence contact validation in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/start`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Start Sequence Contact Validation](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to validate. |
