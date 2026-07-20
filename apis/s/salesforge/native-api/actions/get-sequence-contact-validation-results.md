# Get Sequence Contact Validation Results with Salesforge

Retrieves sequence contact validation results from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/result`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Get Sequence Contact Validation Results](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID with validation results. |
